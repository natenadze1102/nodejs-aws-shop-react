### 1. Link to Task

https://github.com/natenadze1102/nodejs-aws-shop-react

**2. Screenshot**
<img width="1512" alt="image" src="https://github.com/user-attachments/assets/11c3a0c5-bd28-4ea7-86dc-46a32a14806b" />

**3.Deploy**
https://dity7u4qnav41.cloudfront.net
• Opens the React Shop application. You can see the app at /, /cart, etc.

\*\*3.1 Link to S3 bucket
https://sdkinfrastackv2-task2bucket780f9f95-j4jkn9vu78no.s3.eu-central-1.amazonaws.com/

### 4. Date of Completion / Deadline

• Done: 2025-02-15 21:30
• Deadline: 2025-02-15 23:00

**5. Self-Check with Preliminary Score**

Manual Deployment:
• +30 points – S3 bucket was manually created and config’d. The app is manually uploaded and accessible.
• +40 points – CloudFront distribution configured. The site is now served via CloudFront URL. S3 bucket returns 403.
Subtotal so far: 70 points

Automated Deployment:
• +30 points –
• Added CDK scripts (npm run deploy & npm run destroy).
• The S3 bucket & CloudFront distribution are created automatically.
• On deploy, the site is automatically uploaded and invalidation is created.
Subtotal for automated: 30 points

Total: 70 + 30 = 100 points (all requirements done)

6. What Has Been Done?
   • Manual S3 bucket creation & upload. Verified index.html & minor UI changes.
   • Manual CloudFront distribution creation. Confirmed 403 from S3 and valid 200 OK from CloudFront.
   • CDK setup:
   • Created a sdk-infra folder with cdk init --language typescript.
   • Wrote a stack that:
   1. Creates a private S3 bucket (or public, as needed)
   2. Configures a CloudFront distribution with OAI.
   3. Uses BucketDeployment to automatically upload dist/ on npm run deploy.
   4. Invokes CloudFront invalidation automatically.
      • Verified that cdk destroy cleans up everything.
