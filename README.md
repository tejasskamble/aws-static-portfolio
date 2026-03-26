# Cloud Computing & DevOps - Task 1

[cite_start]**Objective:** Host a Static Portfolio on AWS S3 + Serve via CloudFront (HTTPS)[cite: 6].

## Project Links & Deliverables
* [cite_start]**GitHub Repository:** https://github.com/tejasskamble/aws-static-portfolio.git [cite: 25]
* [cite_start]**Secure Hosted URL (CloudFront):** https://d363jckj885tdv.cloudfront.net/ [cite: 26]
* [cite_start]**S3 Bucket Endpoint:** http://tejas-task1-portfolio.s3-website.ap-south-1.amazonaws.com/ [cite: 26]
* [cite_start]**Screenshots:** S3 Bucket Policy & CloudFront Distribution screenshots are included in the submission folder[cite: 27, 28].

---

## Step-by-Step Execution Summary

### 1. Local Development & Git Version Control
* [cite_start]Created a responsive single-page portfolio using `index.html` and `styles.css`[cite: 32].
* [cite_start]Integrated Google Fonts and FontAwesome for UI enhancements[cite: 21].
* [cite_start]Included a Hero section, 3 Project cards, and a Contact footer[cite: 22, 23].
* [cite_start]Initialized a local Git repository and pushed the code to GitHub [cite: 17, 33] using the following commands:
  ```bash
  git init
  git add .
  git commit -m "Initial portfolio commit"
  git branch -M main
  git remote add origin [https://github.com/tejasskamble/aws-static-portfolio.git](https://github.com/tejasskamble/aws-static-portfolio.git)
  git push -u origin main

---

# Cloud Computing & DevOps - Task 2

[cite_start]**Objective:** Containerization Using Docker and Deployment on a Cloud Virtual Machine[cite: 5]. [cite_start]Create a Docker image for the website, run it inside a container, and deploy it on a cloud-based virtual machine[cite: 14, 15, 16].

## Project Links & Deliverables
* **GitHub Repository:** https://github.com/tejasskamble/aws-static-portfolio.git
* **Live Hosted URL (EC2 Public IP):** http://13.233.20.91/
* [cite_start]**Screenshots:** Screenshot of the running container (`docker ps`) is included in the submission folder[cite: 141].

---

## Step-by-Step Execution Summary

### 1. Local Dockerization & Testing
* [cite_start]Created a `Dockerfile` utilizing the lightweight `nginx:alpine` base image[cite: 70].
* [cite_start]Configured the `Dockerfile` to copy local website files into the container at `/usr/share/nginx/html` and exposed port 80 for HTTP traffic[cite: 71, 72].
* [cite_start]Built the Docker image locally using the following command[cite: 82]:
  ```bash
  docker build -t portfolio-website .

  Verified the build by running the container locally and mapping it to port 8080:Bashdocker run -d -p 8080:80 portfolio-website
2. Cloud VM Provisioning (AWS EC2)Launched a new Ubuntu virtual machine instance on AWS EC2.Selected the t2.micro instance type to utilize the Free Tier.Configured the security group to allow inbound HTTP traffic on port 80.Connected to the virtual machine via SSH using the generated .pem key pair:Bashssh -i "maincrafts.pem" ubuntu@13.233.20.91
3. Docker Installation on Cloud VMUpdated the package lists on the Ubuntu server:Bashsudo apt update
Installed Docker securely on the instance:Bashsudo apt install docker.io -y
Started the Docker service:Bashsudo systemctl start docker
Added the ubuntu user to the docker group to execute commands without elevated privileges:Bashsudo usermod -aG docker ubuntu
4. Cloud Deployment & Container ExecutionCloned the project repository directly to the EC2 instance from GitHub:Bashgit clone [https://github.com/tejasskamble/aws-static-portfolio.git](https://github.com/tejasskamble/aws-static-portfolio.git)
Navigated into the project directory (cd aws-static-portfolio).Built the production Docker image directly on the cloud virtual machine:Bashdocker build -t portfolio-website .
Executed the Docker container on the VM, mapping the container's port 80 to the host's port 80 for public access:Bashdocker run -d -p 80:80 portfolio-website
Successfully accessed the live, containerized portfolio via the EC2 instance's public IP address in the browser.
