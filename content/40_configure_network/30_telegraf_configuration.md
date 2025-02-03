---
title: "Telegraf Configuration"
date: 2022-07-14T16:44:50+09:00
weight: 40
pre: "<b>D. </b>"
draft: false
---

{{< line_break >}}
##### 1. To monitor your nodes in Kairos Dashboard, please change the influxdb configuration as below:

###### 1) For both CN and PN,
{{< highlight html >}}
$ grep -A2 "influxdb" /etc/telegraf/telegraf.d/kaia.conf
[[outputs.influxdb]]
urls = [ "http://node.kaia.io:45560" ]
database = "kairos"
{{< /highlight >}}

{{< line_break >}}
If you finish this step, please click the next button ```>``` on the right side of this page.
