# fileprocessorawsS3bucket

# AWS properties 
For aws cloud configuration  add properties like this 
anter your accesskey or secret key from IAM 
if you dont have any dummy user to test it do the bewlo steps
  We need to create new IAM user and give him permission to use only S3 Bucket.
  Let’s create such user. Go to Services -> IAM. In the navigation pane, choose Users and then choose Add user.
  Enter user’s name and check Access type ‘Programatic access’. Press next button. We need to add permissions to this user. Press ‘Attach existing policy directly’, in the search field enter ‘s3’ and among found permissions choose AmazonS3FullAccess
  Then press next and ‘Create User’. If you did everything right then you should see Access key ID and Secret access key for your user. There is also ‘Download .csv’ button for downloading these keys, so please click on it in order not to loose keys.
  
  you can directly copy the access key and secretkey(press show button)
  




amazonProperties:
  endpointUrl: https://s3.us-east-2.amazonaws.com
  accessKey: XXXXXXXXXXXXXXXXX
  secretKey: XXXXXXXXXXXXXXXXx
  bucketName: mynk-bucket



cloud.aws.region.auto: true
cloud.aws.region.static: us-east-2

spring:
    servlet:
      multipart:
       max-file-size: -1
       max-request-size: -1

# post man request 
open postman 
enter the url : localhost:8080/storage/uploadFile
select request as 'post' from the dropdown box
go to 'body' tab
on the radio button select 'formdata'
in key type 'file'
a light drop down will appear 'Text' change it to 'File'
as soon as you chnge it inside the Value column u find a button to upload a file 'Choose Files' 
upload a file 
hit the url  in the response you will get the url path of the uploaded file 
like this : https://s3.us-east-2.amazonaws.com/mynk-bucket/1529514290166-ProdtRgnSzGPI_US_20180614130345_677.dat.gz

