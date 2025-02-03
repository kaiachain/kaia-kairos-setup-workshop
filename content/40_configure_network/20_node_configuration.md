---
title: "Node Configuration"
date: 2022-07-11T17:55:05+09:00
weight: 20
pre: "<b>B. </b>"
draft: false
---

{{< line_break >}}
##### 1. Modify network, discovery and boot node information.
_** Note that CN and PN have some different information._

###### 1) For CN, your configuration should be modified as shown below.
{{< highlight html >}}
$ egrep "^NETWORK|NO_DISCOVER|BOOTNODES|ADDITIONAL" /etc/kcnd/conf/kcnd.conf
NETWORK="baobab"
NETWORK_ID=
NO_DISCOVER=0 # setting 1 to disable discovery
BOOTNODES="kni://979159c738bb0c8c60b36267c56d2b4d4a995326be666460c3d612856caab522ebe6f81ea5cdbb605051f12cbf8f787ce0f172256545a5b3400c751afbdcd0c8@ston36-kairos.node.kaia.io:32323?discport=32323&ntype=bn"
ADDITIONAL="--state.trie-cache-limit 5000 --state.live-pruning"
{{< /highlight >}}

###### 2) For PN
{{< highlight html >}}
$ egrep "^NETWORK|NO_DISCOVER|BOOTNODES|ADDITIONAL" /etc/kpnd/conf/kpnd.conf
NETWORK="baobab"
NETWORK_ID=
NO_DISCOVER=1 # setting 1 to disable discovery
BOOTNODES=""
ADDITIONAL="--state.trie-cache-limit 5000 --state.live-pruning"
{{< /highlight >}}
{{< line_break >}}

##### 2. Check if the static-nodes.json has correct information for your PN.
_** Unlike CN, PN uses a static-nodes.json file to find out where to connect._   
_** If only CN information is found in the file, it is correctly configured._

###### 1) For both PN1 and PN2,
{{< highlight html >}}
[
  "CN_KNI_ADDRESS@CN_INTERNAL_IP:PORT?discport=0&ntype=cn"
]
{{< /highlight >}}


{{< line_break >}}
If you finish this step, please click the next button ```>``` on the right side of this page.
