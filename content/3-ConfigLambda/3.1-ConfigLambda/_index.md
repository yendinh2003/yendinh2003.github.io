---
title : "Config Lambda"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 3.1 </b> "
---
1. Access Lambda and the function you just created  
On the Lambda service interface:  
- On the left side, you’ll see the list of Lambda features. Select **Function**.
- You will see the list of functions you’ve created above, including "fjc-upload-image".
- Click on that function to see an overview of it.  
![Lambda](/images/14.png)

2. Configure Lambda  
- This is where you can enter code to program using **Python** or the language you configured earlier:  
![Lambda](/images/15.png)
- Here, you will enter the code to enable the image analysis function.

- Enter the code in the following structure:

~~~javascript
const AWS = require('aws-sdk');
const s3 = new AWS.S3();
const BUCKET = 'fjc-s3bucket'; // <-- change this to your bucket name

exports.handler = async (event) => {
    try {
        const body = JSON.parse(event.body);
        const imageData = body.image; // base64 image
        const buffer = Buffer.from(imageData, 'base64');
        const fileName = `upload-${Date.now()}.jpg`;

        await s3.putObject({
            Bucket: BUCKET,
            Key: fileName,
            Body: buffer,
            ContentEncoding: 'base64',
            ContentType: 'image/jpeg',
        }).promise();

        return {
            statusCode: 200,
            body: JSON.stringify({ message: 'Upload successful', key: fileName }),
        };
    } catch (error) {
        return {
            statusCode: 500,
            body: JSON.stringify({ error: error.message }),
        };
    }
};
~~~

- After entering the code in the Code Source section as above, you can save your changes by:
  - Clicking the **Deploy** button or using the keyboard shortcut (Ctrl + Shift + U)
  - Wait a few seconds for the system to save your changes and display a success message
  - The result will look like the images below:  
![Lambda](/images/16.png)

You have completed the configuration step for Lambda.