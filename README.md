# Cloud Computing & DevOps - Task 1
**Hosted Portfolio URL:** https://dbpsh2mnll87w.cloudfront.net

## Steps Completed:
1. **Local Development:** Created a responsive single-page portfolio using `index.html` and `styles.css` with Google Fonts and FontAwesome.
2. **Version Control:** Initialized a Git repository and pushed the local code to a public GitHub repository.
3. **AWS S3 Setup:** - Created an S3 bucket and disabled "Block all public access".
   - Attached a Bucket Policy with `s3:GetObject` permission to make the contents publicly readable.
   - Enabled "Static website hosting" and set `index.html` as the default document.
4. **AWS CloudFront (CDN & HTTPS):**
   - Created a new CloudFront distribution using the S3 website endpoint as the origin.
   - Configured the Viewer Protocol Policy to **"Redirect HTTP to HTTPS"** for security.
   - Successfully deployed the distribution to serve the website globally with an SSL/TLS certificate.
