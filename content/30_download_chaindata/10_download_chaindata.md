---
title: "Download the latest Baobab chaindata"
date: 2022-07-11T15:42:53+09:00
weight: 10
pre: "<b>A. </b>"
draft: false
---

{{< line_break >}}
#### 1. Download the latest chaindata snapshot from the Baobab snapshot archive.
##### 0) Before proceeding, please check if your disk space is enough to store and extract the Baobab chaindata.
_** You can refer to the **[Boabab snapshot archive](https://packages.klaytn.net/baobab/chaindata/)** where the Baobab chaindata snapshots have been snapshotted._   
{{< line_break >}}

##### 1) Download the latest one from the archive.
_** Please note that this step will take a long time to download since snapshot is more than 100 GB._
{{< highlight html >}}
$ wget https://packages.klaytn.net/baobab/chaindata/klaytn-baobab-chaindata-latest.tar.gz
{{< /highlight >}}
{{< line_break >}}

##### 3) (Optional) If you are using AWS CLI, _aws s3_ command can be considered to reduce the download time. 
_** This aws s3 command automatically performs multipart uploading and downloading based on the file size. For more details, please refer this link. [S3 multipart upload and download](https://aws.amazon.com/premiumsupport/knowledge-center/s3-multipart-upload-cli)_
{{< highlight html >}}
$ aws s3 cp s3://klaytn-chaindata/baobab/klaytn-baobab-chaindata-20220711010712.tar.gz klaytn-baobab-chaindata-20220711010712.tar.gz
{{< /highlight >}}

{{< line_break >}}
{{< line_break >}}
If you finish this step, please click the next button ```>``` on the right side of this page.
