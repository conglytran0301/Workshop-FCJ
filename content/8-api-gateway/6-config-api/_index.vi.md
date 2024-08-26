+++
title = "Cấu hình API"
date = 2020-05-14T00:38:32+07:00
weight = 6
chapter = false
pre = "<b>8.6 </b>"
+++

#### Cấu hình API

1. Trong giao diện **API**

- Chọn **Stages**
- Chọn **Dev**
- Copy **Invoke URL** `https://7s5pb02ska.execute-api.ap-southeast-1.amazonaws.com/Dev`

![18-API](/images/9/9-api-18.png?width=90pc)

2. Trong giao diện **code web**

- Tìm file **api.js**
- Dán **Invoke URL** vào dòng số 8 và thêm `/serverless` phía sau.

![20-API](/images/9/9-api-20.png?width=90pc)

- Lưu lại và upload lên **S3**
