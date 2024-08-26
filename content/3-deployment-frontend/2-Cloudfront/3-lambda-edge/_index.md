+++
title = "Lambda@Edge Configuration for Origin Website"
date = 2020-05-14T00:38:32+07:00
weight = 3
chapter = false
pre = "<b>2.2.3 </b>"
+++

#### Lambda@Edge Configuration for Origin Website

1. In the **Cloudfront** interface

- Select **Functions**
- Select **Create function**

![16-Cloudfront](/images/4/4-cloudfront-16.png?width=90pc)

2. In the **Create function** interface

- Enter **Name**: `fcj-lambda-edge`
- In the Runtime section, select cloudfront-js-2.0
- Select **Create function**

![17-Cloudfront](/images/4/4-cloudfront-17.png?width=90pc)

3. In the **Functions** interface

- Select the **Functions** that you just created

![18-Cloudfront](/images/4/4-cloudfront-18.png?width=90pc)

- Scroll down to the **Build** section
- In the **Function code** section, select **Development**
- Copy this code to:

```
function handler(event) {
    var request = event.request;
    var uri = request.uri;

    // Check whether the URI is missing a file name.
    if (uri.endsWith('/')) {
        request.uri += 'index.html';
    }
    // Check whether the URI is missing a file extension.
    else if (!uri.includes('.')) {
        request.uri += '/index.html';
    }

    return request;
}
```

- Then select **Save changes**

![19-Cloudfront](/images/4/4-cloudfront-19.png?width=90pc)

- Go to **Publish**
- Select **Publish function**

![20-Cloudfront](/images/4/4-cloudfront-20.png?width=90pc)

4. Return to the **Distributions** interface

- Select the **Distributions** you created
- Select **Behaviors**
- Select Behavior with origin forward to your S3
- Then select **Edit**

![21-Cloudfront](/images/4/4-cloudfront-21.png?width=90pc)

5. In the **Edit** interface

- Scroll down to find **Function associations- optional**
- Configuration with **Viewer request**
- **Function type** select **CloudFront Functions**
- **Function ARN/Name** select **fcj-lambda-edge** you just created above
- Select **Save changes**

![22-Cloudfront](/images/4/4-cloudfront-22.png?width=90pc)
