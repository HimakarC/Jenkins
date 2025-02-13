# Jenkins

--> The very first thing to use Jenkins is to install Java <br>

### To install Java
sudo apt update <br>
sudo apt install openjdk-17-jdk -y <br>
java -version  # Verify Java installation <br>

### After installing java, need to add Jenkins Repository
wget -O - https://pkg.jenkins.io/debian-stable/jenkins.io.key | sudo tee \
  /usr/share/keyrings/jenkins-keyring.asc > /dev/null <br>
echo "deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
  https://pkg.jenkins.io/debian-stable binary/" | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null

### Now install Jenkins
sudo apt update <br>
sudo apt install jenkins -y <br>

### Now start Jenkins and Enable it to use
sudo systemctl start jenkins <br>
sudo systemctl enable jenkins <br>
sudo systemctl status jenkins <br>

--> Now, by default port 8080 is allocated for using Jenkins, use public IP of EC2 instance and login to it. <br>

### To get the Admin Password
sudo cat /var/lib/jenkins/secrets/initialAdminPassword
