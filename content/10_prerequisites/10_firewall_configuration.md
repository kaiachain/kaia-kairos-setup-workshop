---
title: "Firewall Configuration"
date: 2022-07-11T19:18:45+09:00
weight: 10
pre: "<b>A. </b>"
draft: false
---
{{< line_break >}}

##### 1. *(Only for CN)* Firewall configuration

###### 1) If Private Network performance test is completed, remove below Kaia CN's IP address of Private Network from your firewall ingress rule.
```Pre Cyprss KF CN IP```
```Pre Cyprss KF BN IP```

###### 2) For communication and multichannel between Kairos CN, allow TCP ```32323-32324``` with below IP addresses to your firewall ingress rule.
```34.64.63.34```   
```34.64.209.150```   
```34.64.229.190```   
```34.64.63.183```
```147.92.173.41```

###### 3) Additionally, it is required to allow UDP ``` 32323 ``` with the same IP addresses to your firewall ingress rule.
```34.64.155.25```   

###### 4) For communication, allow ```all traffic``` to your firewall ```egress``` rule.
```vim
IP version    |    Type           |    Protocol    |    Port range    |    Destination
---------------------------------------------------------------------------------------
IPv4          |    All traffic    |    All         |    All           |    0.0.0.0/0
```

{{< line_break >}}   
*Please note that the above four IP addresses are attached to the Kaia Kairos CNs.*

{{< line_break >}}
If you finish this step, please click the next button ```>``` on the right side of this page.
