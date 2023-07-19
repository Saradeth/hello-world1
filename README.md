## DevOps Project for Beginners   

![DevOps Flow](https://github.com/Saradeth/hello-world1/assets/15135398/86b8a81b-c06c-4a4a-9c93-585d34d5d783)
Instal Jenkins
1. Go to Jenkins's Website https://www.jenkins.io/download/
   -> Choose Red Hat/Fedora/Alma/Rocky/CentOS
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
7. New item --> input name (HelloWorldJob--> Freestyl project --> OK --> input the description
8. Build chose Execute shell
echo "Hello World"
uptime
9. Integration Git with Jenkins
10. Go to Jenkins server -->
cat /etc/hostname
hostname jenkins-server

11. Install Git
yum install git

git --version

whereis git

12. Install github plugin in Jenkins web --> config git
13. creat new iteam --> PullCodeFromGitHub --> Freesyle project --> OK --> Source code Management --> Git
14. Go to Jenkins server
cd /var/lib/jenkins/workspace
16. Integrate Maven with Jenkins
cd /opt
wget https://dlcdn.apache.org/maven/maven-3/3.9.3/binaries/apache-maven-3.9.3-bin.tar.gz
tar -xvzf apache-maven-3.9.3-bin.tar.gz
mv apache-maven-3.9.3 maven
cd /maven
cd /bin
./mvn -v
17. cd ~
ll -a

Find Java home directory
find / -name java-11*

vi .bash_profile
- M2_HOME=/opt/maven
- M2=/opt/maven/bin
- JAVA_HOME=/usr/lib/jvm/
- PATH=$PATH:$HOME/bin:$JAVA_HOME:$M2_HOME:$M2
- save
echo $PATH

source .bash_projile
mvn -v

18. Install Maven plugin in Jenkins web
19. confige
JDK
/usr/lib/jvm/java-11

Maven
maven-3.9.3
/opt/maven
--> apply and save
20. Create new item --> FirstMavenProject --> Maven project --> OK
Git
URL git repositry
clean install --> Apply --> Save

Go to Jenkins server
cd /var/lib/jenkins/
ll
cd workspace/
ll
cd FirstMavenProject
ll


