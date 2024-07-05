Launching a static website on Amazon S3

I've hosted a static website using Amazon S3 and Amazon Route 53.

The information about how to build this project was found from 
Lucy Wang her YouTube channel is, @TechwithLucy.  
I have chosen to make my documentation of this project appropriately granular to help anybody who may choose to do this project.

Step#1

Open the AWS management console and select Route 53 service from the search bar.

Select registered domains, type the domain name you want to purchase, and enter your address details. 
Now you can accept the terms and conditions and complete the order.

Step#2

Go to the Amazon S3 page and create a bucket.
Give the bucket the same name as your registered domain.
Ensure that “block or public access” is deselected to ensure the bucket is publicly accessible via the Internet
Acknowledge the warning, leave all of the other settings the same, and select create bucket.
Select your new bucket and upload the file
Upload html file for static website.

 
To ensure the bucket is enabled for static website hosting and has the correct permissions

Scroll to the bottom of the page labeled “static website hosting”-
which is disabled by default. You must now enable this.

Type in the name of your uploaded index document and save the changes

Now go back to the permissions tab attach a bucket policy by selecting edit, and save changes.
 
The sample website is now publicly accessible for viewers, through the Amazon provider URL. 
Now you must route your purchased domain to your S3 bucket.


Step #3

Go back to route 53 select hosted zones and select domain. And create a record to ensure bucket is connected to the route 53 domain name. This can be done by selecting create record and select simple routing policy and select next.
 
Select define simple records

In the values sections select alias to S3 website end point.
Select the region where you hosted your bucket and select the S3 and point.
Deselect “Evaluate target health” and select simple records.
 
Confirm by selecting create records.
 
You can now review my static website at:
http://cloudcomputingdemo.com

