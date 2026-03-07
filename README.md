# Cloud Computing & DevOps - Task 1

[cite_start]**Objective:** Host a Static Portfolio on AWS S3 + Serve via CloudFront (HTTPS)[cite: 6].

## Project Links & Deliverables
* [cite_start]**GitHub Repository:** https://github.com/tejasskamble/aws-static-portfolio.git [cite: 25]
* [cite_start]**Secure Hosted URL (CloudFront):** https://dbpsh2mnll87w.cloudfront.net/ [cite: 26]
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
