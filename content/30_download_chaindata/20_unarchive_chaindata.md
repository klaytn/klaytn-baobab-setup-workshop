---
title: "Extract the chaindata"
date: 2022-07-11T15:43:06+09:00
weight: 20
pre: "<b>B. </b>"
draft: false
---

{{< line_break >}}
##### 2. Extract the chaindata downloaded to the DATA_DIR.

###### 1) For CN,
{{< highlight html >}}
$ tar -C <your_kaia_home_path>/kcnd/data -xvf kaia-kairos-pruning-chaindata-20240819010812.tar.gz --exclude klay/chaindata/receipts
{{< /highlight >}}

###### 2) For PN,
{{< highlight html >}}
$ tar -C <your_kaia_home_path>/kpnd/data -xvf kaia-kairos-pruning-chaindata-20240819010812.tar.gz --exclude klay/chaindata/receipts
{{< /highlight >}}

_** If you want to reduce the time for extracting, please refer this [pigz](https://zlib.net/pigz/) example._
{{< highlight html >}}
(Amazon Linux 2) $ sudo amazon-linux-extras install epel
(CentOS) $ sudo yum install epel-release -y
$ sudo yum install pigz
$ tar -I pigz -C <your_kaia_home_path>/k*nd/data -xvf kaia-kairos-pruning-chaindata-20240819010812.tar.gz --exclude klay/chaindata/receipts
{{< /highlight >}}

{{< line_break >}}
If you finish this step, please click the next button ```>``` on the right side of this page.