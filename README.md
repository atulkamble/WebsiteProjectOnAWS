# WebsiteProjectonAWS
Project: Host a Website on AWS
Admin >>

1) Create Architecture

Software: https://www.drawio.com/

2) Sign up for Github

https://github.com/

3) Create Repository

4) Naviagte to IAM >> Create User Group (Developers) | Add user (developer) to User GroupCretate user account (developer) | EC2 Full Access Policy. | Create Console Credentials. Shared sign in details to developer.

5) Create ec2 instance. (SG: ssh, http, https) 

6)

Developer >>

1) Sign in to Account.

2) ssh to EC2 Instance.

```
ssh -i "key.pem" ec2-user@ec2-3-108-254-82.ap-south-1.compute.amazonaws.com
```
3) 
```
sudo yum update -y
sudo yum install httpd -y
sudo systemctl start httpd
sudo systemctl enable httpd
sudo usermod -a -G apache ec2-user
sudo chmod 777 /var/www/html
cd /var/www/html
touch index.html
sudo nano index.html
cat index.html
history
```
4) Check public ip of instance in web-browser
```
http://3.108.254.82/
```
