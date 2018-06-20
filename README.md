# fileprocessorawsS3bucket

# 

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

