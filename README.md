Launching a static website on Amazon S3

I have hosted a static website using Amazon S3 and Amazon route 53.

The information about how to build this project was found from 
Lucy Wang her YouTube channel is, @TechwithLucy.  
I have chosen to make my documentation of this project appropriately granular to help anybody that may choose to do this project.

Step#1

Open the AWS management console and select Route 53 service from the search bar.

Select registered domains and type the domain name you would like to purchase, end to your address details and accept the terms and conditions and complete the order.

Step#2

Go to the Amazon S3 page create a bucket.
Give the bucket the same name as your registered domain.
Ensure that “block or public access” is deselected to ensure the bucket is publicly accessible via the Internet
Acknowledge the warning leave all of settings the same and select create bucket.
Select your new bucket and upload file
Upload html file for static website.

 
To ensure bucket is enabled for static website hosting and has the correct permissions

Scroll to the bottom of the page labelled “static website hosting”-
which is disabled by default. You must now enable this.

And type in the name of your uploaded index document and save changes

Now go back to permissions tab. And attach a bucket policy by selecting edit, and save changes.
 
The sample website is now publicly accessible for viewers, through the Amazon provider URL. Now you must read the words your purchase domain to your S3 bucket.


Step #3

Go back to route 53 select hosted zones and select domain. And create a record to ensure Bucky is connected to the route 53 domain name. This can be done by selecting create record and select simple routing policy and select next.
 
Select define simple records

In values sections select alias two S3 website end point.
Select the region where you hosted your bucket and select the S3 and point.
Deselect “Evaluate target health” and select simple records.
 
Confirm by selecting create records.
 
You can now review my static website at:
http://cloudcomputingdemo.com/
