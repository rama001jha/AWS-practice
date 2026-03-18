<h1>Jenkins Setup on AWS EC2</h1>

<p>
In this project, I created an AWS EC2 instance and installed Jenkins on it.
Jenkins is used for automation like building and deploying applications.
</p>

<hr>

<h2>Steps I Followed</h2>

<h3>1. Launch EC2 Instance</h3>
<ul>
  <li>Created an EC2 instance from AWS Console</li>
  <li>Selected Ubuntu as OS</li>
  <li>Allowed ports 22 (SSH) and 8080 (Jenkins)</li>
</ul>

<h3>2. Connect to Instance</h3>
<pre>
ssh -i your-key.pem ubuntu@your-public-ip
</pre>

<h3>3. Install Java</h3>
<pre>
sudo apt update
sudo apt install openjdk-21-jdk -y
</pre>

<h3>4. Install Jenkins</h3>
<pre>
curl -fsSL https://pkg.jenkins.io/debian/jenkins.io.key | sudo tee \
/usr/share/keyrings/jenkins-keyring.asc > /dev/null

echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
https://pkg.jenkins.io/debian binary/ | sudo tee \
/etc/apt/sources.list.d/jenkins.list > /dev/null

sudo apt update
sudo apt install jenkins -y
</pre>

<h3>5. Start Jenkins</h3>
<pre>
sudo systemctl start jenkins
sudo systemctl enable jenkins
</pre>

<h3>6. Access Jenkins</h3>
<pre>
http://your-public-ip:8080
</pre>

<h3>7. Get Password</h3>
<pre>
sudo cat /var/lib/jenkins/secrets/initialAdminPassword
</pre>

<hr>

<h2>Result</h2>
<p>
Jenkins was successfully installed and accessed in the browser.
</p>

<hr>

