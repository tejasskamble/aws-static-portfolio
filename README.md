# Cloud Computing & DevOps - Task 1: Host a Static Portfolio on AWS S3 + Serve via CloudFront (HTTPS)

## Project Links
* **GitHub Repository:** https://github.com/tejasskamble/aws-static-portfolio.git
* **Secure Hosted URL (CloudFront):** https://dbpsh2mnll87w.cloudfront.net/
* **S3 Bucket Endpoint:** http://tejas-task1-portfolio.s3-website.ap-south-1.amazonaws.com/

## Objective
[cite_start]To build a responsive single-page portfolio and host it on AWS S3, secured with CloudFront (HTTPS)[cite: 9, 20].

## Detailed Step-by-Step Execution

### Step 1: Local Web Development
* Created a responsive single-page portfolio locally containing `index.html` and `styles.css`.
* [cite_start]Included a Hero section with a CTA button, an About section, 3 Project cards, and a Contact footer[cite: 20, 22, 23].
* [cite_start]Integrated Google Fonts and FontAwesome for typography and icons[cite: 21].

### Step 2: Version Control (Git & GitHub)
* [cite_start]Initialized a local Git repository to store code and show version history[cite: 17].
* Executed the following commands to push the code to a public GitHub repository:
  ```bash
  git init
  git add .
  git commit -m "Initial portfolio commit"
  git branch -M main
  git remote add origin [https://github.com/tejasskamble/aws-static-portfolio.git](https://github.com/tejasskamble/aws-static-portfolio.git)
  git push -u origin main
