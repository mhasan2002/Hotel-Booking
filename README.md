# Hotel-Booking
**Step#01
	Check IPV4 address of Instance
Step#02
	Click on Instance Id
Step#03
	Click Connect
Step#04
	Under the heading of Example, copy the commmand 
ssh -i "your_key.pem" ubuntu@ec2-15.-15-689-92.compute.amazaonaws.com

Step#05 
	Once access is granted to the EC2 instance, run the command
ssh-keygen

Step#06
	write in the command 
cd ~/.ssh
and then type "ls" 
to find the ".pub" file 

Step#07
	write the command
"cat file_name.pub" to see the content of this file and then copy it

Step# 08
	Now, open github profile, select your picture in the top-right corner. Scroll down to settings and click it

Step# 09
	In the settings panel, search for SSH AND GPG Keys on the panel on left hand-size

Step# 10
	Click the SSH Keys and add a new SSH Key. Add a title and paste the key

Step# 11 
	Comeback to the cloud shell, to verify, type in the command 
ssh git@github.com

Step# 12
	now, install the apache2 server on the ec2 instance. 
Type in the command
	1. sudo su (to grant super user access)
	2. sudo apt install apache2

Step# 13
	Now, start the service of apache2
run the commands
	1. systemctl start apache2
	2. systemctl enable apache2
	3. sysatemctl status apache2

step# 14
	Refresh the IPV4 address page on the browser to check the apache homepage

Step# 15
	copy the path to the html from the homepage 
/var/www/html

Step# 16
	go to the desired directory i.e (/var/www/html)

Step# 17 -- If using GITHUB
	type "ls" 
there should be only one file named 'index.html' in the folder

Step# 18 
	now, go back to the github profile, click your repository, then click "CODE" on the right side and copy the link under SSH

Step# 19
	comeback to the console, run the command still being in the directory /var/www/html
Command:
	git clone your_repo_SSH_link.com

Step# 20
	now, write in the command to move the contents from your folder into html folder
example we have this content in the html folder

index.html   makaan

write the command
mv makaan/* .

to move the contents from the folder of makaan to HTML folder


Step#21
	Finally, refresh the IPV4 address page 





Incase of getting the contents from the S3-Bucket
in Step # 17

Go to the s3 bucket and copy the object url of your uploaded folder
then,
run this command instead of (git clone) 

wget your_object_url.com

now, if the folder is zipped,
run the command 

sudo apt install unzip

then, the contents in the HTML folder would look like this

HTML
|-------> index.html
|-------> your_folder.zip

run the command

unzip your_folder.zip


Finally, refresh the IPV4 address page**
