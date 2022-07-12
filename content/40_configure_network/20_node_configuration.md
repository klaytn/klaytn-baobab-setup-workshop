---
title: "Node Configuration"
date: 2022-07-11T17:55:05+09:00
weight: 20
pre: "<b>B. </b>"
draft: false
---

{{< line_break >}}
#### 1. Modify network, discovery and boot node information.
_** Note that CN and PN have some different information._

##### 1) For CN,
{{< highlight html >}}
$ egrep "^NETWORK|NO_DISCOVER|BOOTNODES" /etc/kcnd/conf/kcnd.conf
NETWORK="baobab"
NETWORK_ID=
NO_DISCOVER=0 # setting 1 to disable discovery
BOOTNODES="kni://8e1881cdca97f52a76c6d2683db030f51a34ffc039476b4ed5bc5c757de1b5ce48fea1e53aa182a6ac2b076460881d50d3b57461d1cf36fae777e992893ad485@52.199.8.244:32323?discport=32323&ntype=bn"
{{< /highlight >}}

##### 2) For PN,
{{< highlight html >}}
$ egrep "^NETWORK|NO_DISCOVER|BOOTNODES" /etc/kpnd/conf/kpnd.conf
NETWORK="baobab"
NETWORK_ID=
NO_DISCOVER=1 # setting 1 to disable discovery
BOOTNODES=""
{{< /highlight >}}
{{< line_break >}}

#### 2. Check if the static-nodes.json is correct for your PN.
_** Unlike CN, PN uses a static-nodes.json file to find out where to connect. The file might be already generated during installation of the Pre-cypress, then you don't need to create or change anything. This step is just required to confirm if the information is correct._

##### 1) For PN1,
{{< highlight html >}}
[
"CN_KNI_ADDRESS@CN_INTERNAL_IP:PORT?discport=0&ntype=cn",
"PN2_KNI_ADDRESS@PN2_INTERNAL_IP:PORT?discport=0&ntype=pn"
]
{{< /highlight >}}

##### 2) For PN2,
{{< highlight html >}}
[
"CN_KNI_ADDRESS@CN_INTERNAL_IP:PORT?discport=0&ntype=cn",
"PN1_KNI_ADDRESS@PN1_INTERNAL_IP:PORT?discport=0&ntype=pn"
]
{{< /highlight >}}


{{< line_break >}}
If you finish this step, please click the next button ```>``` on the right side of this page.
