---
title: "replace_bls-nodekey"
date: 2022-07-11T15:17:04+09:00
weight: 30
pre: "<b>C. </b>"
draft: false
---

{{< line_break >}}
#### 4. Replace bls-nodekey on the CN - Except Bughole & Certik.

> BLS-Nodekey is your Private key what you generate with Klay Tool.

![CN](https://raw.githubusercontent.com/klaytn/klaytn-pre-cypress-setup-workshop/main/static/images/nodekey.png)

In order to operate a node, a `bls-nodekey` is required. The KCN binary will create a new one for you if you do not have it. {{< line_break >}}
If you have one, you need to put your `bls-nodekey` into the `data` directory.

##### 1) Delete auto-generated bls-key
{{< highlight html >}}
$ mv /var/kcnd/data/bls-nodekey /var/kcnd/data/bls-nodekey_temp
{{< /highlight >}}

{{< line_break >}}

##### 2) Create bls-nodekey file
{{< highlight html >}}
$ vi /var/kcnd/data/bls-nodekey
{{< /highlight >}}


{{< line_break >}}
{{< line_break >}}

{{< line_break >}}
If you finish this step, please click the next button ```>``` on the right side of this page.
