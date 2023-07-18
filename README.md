## DevOps Project for Beginners   

![DevOps Flow](https://github.com/Saradeth/hello-world1/assets/15135398/86b8a81b-c06c-4a4a-9c93-585d34d5d783)

1. Go to Jenkins's Website https://www.jenkins.io/download/
2. Choose Red Hat/Fedora/Alma/Rocky/CentOS
3. Go to Jenkins server and past 
sudo wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat-stable/jenkins.repo
sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io-2023.key

yum install fontconfig java-11-openjdk
yum install jenkins

4. check service Jenkins
service jenkins status
service jenkins start

5. Open this file from Jenkins web
cat /var/lib/jenkins/secrets/initialAdminPassword
6. Copy password and past in Jenkins server --> Continue
7. New item --> input name --> Freestyl project --> OK --> input the description
8. Build chose Execute shell
echo "Hello World"
uptime
9. Integration Git with Jenkins
10. Go to Jenkins server -->
cat /etc/hostname
hostname jenkins-server

11. In


