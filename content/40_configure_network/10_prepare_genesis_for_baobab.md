---
title: "Prepare genesis.json for Baobab network"
date: 2022-07-11T17:10:58+09:00
weight: 10
pre: "<b>A. </b>"
draft: false
---

{{< line_break >}}
#### 1. Remove or backup existing genesis.json for Pre-cypress.
##### 1) For CN,
{{< highlight html >}}
$ mv <your_klaytn_home_path>/kcnd/data/genesis.json <your_klaytn_home_path>/kcnd/data/genesis.json.pre-cypress 
{{< /highlight >}}
##### 2) For PN,
{{< highlight html >}}
$ mv <your_klaytn_home_path>/kpnd/data/genesis.json <your_klaytn_home_path>/kpnd/data/genesis.json.pre-cypress
{{< /highlight >}}
{{< line_break >}}

#### 2. Download the genesis.json for Baobab network.
##### 1) For CN,
{{< highlight html >}}
$ curl -X GET https://packages.klaytn.net/baobab/genesis.json -o <your_klaytn_home_path>/kcnd/data/genesis.json
{{< /highlight >}}
##### 2) For PN,
{{< highlight html >}}
$ curl -X GET https://packages.klaytn.net/baobab/genesis.json -o <your_klaytn_home_path>/kpnd/data/genesis.json
{{< /highlight >}}
{{< line_break >}}

#### 3. Check the network_id in the genesis.json downloaded.
##### 1) For CN,
{{< highlight html >}}
$ grep "chainId" <your_klaytn_home_path>/kcnd/data/genesis.json
"chainId": 1001,
{{< /highlight >}}
##### 2) For PN,
{{< highlight html >}}
$ grep "chainId" <your_klaytn_home_path>/kpnd/data/genesis.json
"chainId": 1001,
{{< /highlight >}}
{{< line_break >}}

{{< line_break >}}
If you finish this step, please click the next button ```>``` on the right side of this page.
