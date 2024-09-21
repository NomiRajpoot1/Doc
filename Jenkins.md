
# Jenkins
## Jenkins installation :







1. Install Java

```bash
  sudo apt install openjdk-11-jdk -y

```
You can verify the installation by checking the Java version:
```bash
  java -version
```


2. Add Jenkins Repository 
 Add the GPG key:


```bash
  curl -fsSL https://pkg.jenkins.io/debian/jenkins.io-2023.key | sudo tee \
/usr/share/keyrings/jenkins-keyring.asc > /dev/null

```

Add the Jenkins repository:


```bash
  echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
https://pkg.jenkins.io/debian binary/ | sudo tee \
/etc/apt/sources.list.d/jenkins.list > /dev/null

```

3. Install Jenkins
```bash
  sudo apt update
  sudo apt install jenkins -y

```
4. Start and enable Jenkins
```bash
  sudo systemctl start jenkins
  sudo systemctl enable jenkins

```
5. Open firewall ports (if applicable)
```bash
  sudo ufw allow 8080
  sudo ufw allow OpenSSH
  sudo ufw enable
```
6. Access Jenkins
```bash
    http://your_server_ip_or_domain:8080

```
7. Unlock Jenkins
```bash
  sudo cat /var/lib/jenkins/secrets/initialAdminPassword

```
