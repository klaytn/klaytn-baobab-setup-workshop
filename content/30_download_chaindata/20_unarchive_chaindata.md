---
title: "Extract the chaindata"
date: 2022-07-11T15:43:06+09:00
weight: 20
pre: "<b>B. </b>"
draft: false
---

{{< line_break >}}
#### 1. Extract the chaindata downloaded to the DATA_DIR.

##### 1) For CN,
{{< highlight html >}}
$ grep "DATA_DIR" /etc/kcnd/conf/kcnd.out
$ tar -C <your_klaytn_home_path>/kcnd/data -xvf klaytn-baobab-chaindata-latest.tar.gz
{{< /highlight >}}
_** If you don't remember the path DATA_DIR, you can check kcnd.conf._
{{< line_break >}}

##### 2) For PN,
{{< highlight html >}}
$ grep "DATA_DIR" /etc/kpnd/conf/kpnd.out
$ tar -C <your_klaytn_home_path>/kpnd/data -xvf klaytn-baobab-chaindata-latest.tar.gz
{{< /highlight >}}
_** If you don't remember the path DATA_DIR, you can check kpnd.conf._

#### 2. You can remove the chaindata downloaded, if the previous step is completed.

##### 1) For both CN and PN,
{{< highlight html >}}
$ rm klaytn-baobab-chaindata-latest.tar.gz
{{< /highlight >}}

{{< line_break >}}
{{< line_break >}}
{{< line_break >}}
If you finish this step, please click the next button ```>``` on the right side of this page.
