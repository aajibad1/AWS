#Creating a CloudFront distribution to speedup our website

Go to AWS Console


Click CloudFornt service.


Click create Distribution.


Click Web.


Enter the public DNS of Ec2 instance. (Note: you have to go to EC2 Service to get the public DNS)


Leave everything default and go to Default cache behaviour settings.



In allowed HTTP method select the option with get,post,put,delete..etc.


Leave everything default and go to Distribution Settings.



In the default root object enter your starting page. (For example: index.php)


Now, click create distribution.


Wait for atleast 20-40 mins till the Distribution gets to Deployed status.



When the deployed status is reached, use the cloudfront domain name to see the website with a great speed.

