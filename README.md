# WebsiteProjectonAWS
Project: Host a Website on AWS

## Admin Roles and Responsiblity

1) Create Architecture using Software: https://www.drawio.com/
2) Sign up for Github: https://github.com/
3) Create Repository
4) Naviagte to *IAM* >> Create *User* - dev | Create *User Group* (Developers) | Add user (dev) to User Group (Developers) | Add Permisions >> Attach Policy >> Assign EC2 Full Access Policy. | Naviagte to Security Credentials | Enable Console Access | Generate Password. Shared sign in details to developer.
5) Create ec2 instance. (SG: ssh, http, https) 
6) deploy following packages and configure webserver.
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
7) Upload Website Code
//  Install and configure Git
```
sudo yum install git
git --version
```
// Set user details 
```
git config --global user.name "FirstName LastName"
git config --global user.email abc@gmail.com
```
OR 

Setup Github Desktop
https://desktop.github.com/

```
git clone https://github.com/prasadkashid24/Portfolio.git
cd Portfolio
mv /* /var/www/html
```

## Developer Responsibility

1) Sign in to Account.
2) ssh to EC2 Instance.
```
ssh -i "key.pem" ec2-user@ec2-3-108-254-82.ap-south-1.compute.amazonaws.com
```
3) Navigate to cd /var/www/html and maintain code.
4) Check public ip of instance in web-browser
```
http://3.108.254.82/
```
