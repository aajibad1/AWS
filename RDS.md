#Creating an instance for database using RDS

Go on AWS management Console.

Then click Services.



Then click RDS.


In the left panel select Subnet Groups.

Click on create DB Subnet group.


Enter the name and description for it.


Select the VPC id from the drop down.


Now click on add all subnet.


Now click Create.


Now from the left panel click on Instances.

Click on launch DB Instance.


Select MySql or the database of your choice and click next. (Here we will use mysql database for the demo)


Click dev/test and next step.

Select the instance of your type.


In Multi-AZ deployment, Select No option.


Then, in storage type according to your need.


Enter the Database identifier and other details. (Please note it down somewhere because we would need this)


Click Next.


Select the default VPC.


Select the subnet group that we created.


Set publically accessible to NO.

(For this step you need to go to VPC service and copy your VPC CIDR)

Now create a new security group and add a rule.


Select type Mysql/Aurora-->portrange will be 3306-->type the VPC CIDR in source.


Click create.


Now leave everything default and then click Launch DB Instance.


Now we have created an DB instance.



Download and install mysql Workbench.

Now open it.


Create a new connection by clicking on '+'.


Enter the connection name of your choice.


In connection method option Select Standard TCP/IP over SSH.


Now Go to AWS console and select EC2 service and then copy your public DNS.

Now comeback to the workbench settings and paste it in the ssh hostname.


Then, enter the ssh username ec2-user.


In ssh key file, point it to the file that we downloaded.


Now, go back to AWS console and select RDS service.


Select your database instance and copy the endpoint.


Now, comeback to Mysql Workbench and paste it in mysql hostname.


Enter server port number 3306.


Enter the username that you had entered while creating the DB Instance for your database.


(If you don't remember the username go to RDS service and select your instance and then click on instance actions and then see details)

Enter the password for it.


Now click on test connection to test it.


If connection was successful click ok.


Now, we have established a very secure connection to our database instance.



Now, Create a new database and name it whatever you want. (No need to create a new one if you have already created)


In the Left panel select import/restore.


Then select import from Self contained file and point it to our database.


In default target schema, select the schema of your choice and click start import.


Now, we have imported the database and now you can make changes to the database.
