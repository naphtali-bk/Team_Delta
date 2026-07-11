# 🚀 Project Implementation

As part of the **Cloud Build With Peers** initiative, Team Delta collaborated to design, build, and deploy a static portfolio website on AWS. We followed AWS best practices for securing cloud resources before deploying the application. Throughout the project, we worked together by brainstorming ideas, sharing tasks, reviewing each other's work, and documenting our progress.

## Step 1: Set Up the AWS Account

Before deploying any resources, we ensured that our AWS environment was properly configured.

- Created an AWS account.
- Verified the account.
- Signed in to the AWS Management Console.
- Familiarized ourselves with the AWS Free Tier services used for the project.

![Folder Format](shots/Day%201/image2.png)

---

## Step 2: Secure the AWS Account

Security was our first priority before provisioning any AWS resources.

### Enable Multi-Factor Authentication (MFA)

To protect the AWS account, we enabled Multi-Factor Authentication (MFA) on the root user account.

The process involved:

- Navigating to **Security Credentials** in the AWS Management Console.
- Selecting **Assign MFA Device**.

  ![Folder Format](shots/Day%201/image5.png)

- Registering an authenticator application.

  ![Folder Format](shots/Day%201/image6.png)

- Verifying the generated authentication codes.

  ![Folder Format](shots/Day%201/image7.png)

Enabling MFA provides an additional layer of security by requiring a second form of authentication during sign-in.

  ![Folder Format](shots/Day%201/image8.png)

---

## Step 3: Create an IAM Administrator User

Following AWS security best practices, we avoided using the root account for everyday tasks.

Instead, we:

![Folder Format](shots/Day%201/image9.png)

- Created an IAM user.

![Folder Format](shots/Day%201/image10.png)

- Enabled AWS Management Console access.

![Folder Format](shots/Day%201/image11.png)

- Created an Administrator group.

![Folder Format](shots/Day%201/image12.png)

- Attached the **AdministratorAccess** policy.

![Folder Format](shots/Day%201/image11.png)

- Added the IAM user to the Administrator group.

![Folder Format](shots/Day%201/image12.png)
![Folder Format](shots/Day%201/image14.png)

- Signed in using the IAM user for the remainder of the project.

![Folder Format](shots/Day%201/image15.png)

This approach protects the root account and promotes secure access management.

---

## Step 4: Prepare the Portfolio Website

As a team, we designed a simple static portfolio website to introduce Team Delta and highlight our AWS learning journey.

The website includes:

- Hero section
- Team introduction
- AWS Builder Challenge overview
- Fun facts
- Contact section

 ![Folder Format](shots/Day%202/image1.png)

---

## Step 5: Create an Amazon S3 Bucket

We created an Amazon S3 bucket to host the static website.

![Folder Format](shots/Day%202/image4.png)

The bucket was configured with:

- A globally unique bucket name

![Folder Format](shots/Day%202/image2.png)

- Appropriate AWS Region

- Default storage settings

![Folder Format](shots/Day%202/image3.png)

---

## Step 6: Upload Website Files

We uploaded the website files to the S3 bucket, including:

- `index.html`
- `styles.css`
- `profile-photo.svg`

 ![Folder Format](shots/Day%203/image2.png)

---

## Step 7: Enable Static Website Hosting

We enabled Static Website Hosting on the S3 bucket and configured:

- **Index document:** `index.html`
- **Error document:** `index.html`

AWS then generated a static website endpoint that allowed us to access the deployed website.

---

## Step 8: Configure CloudFront

To improve performance and security, we created an Amazon CloudFront distribution.

![Folder Format](shots/Day%204/image5.png)

The configuration included:

- Amazon S3 as the origin
- `index.html` as the default root object

![Folder Format](shots/Day%204/image1.png)

- Redirecting HTTP requests to HTTPS

![Folder Format](shots/Day%204/image4.png)

- Enabling waf (Web Application Firewall) for enhanced security

![Folder Format](shots/Day%204/image6.png)

- Content compression for improved performance

![Folder Format](shots/Day%204/image7.png)

CloudFront distributes the website through AWS edge locations, reducing latency for users around the world.

- Accessing the website through the CloudFront distribution URL

![Folder Format](shots/Day%204/image8.png)

---

## Step 9: Test the Deployment

After deployment, we validated that:

- The website loaded successfully.
- Styling and images displayed correctly.
- HTTPS was working.
- Navigation links functioned correctly.
- The website was accessible through the CloudFront distribution.

![Folder Format](shots/Day%204/image8.png)

---



## Step 6: Create a GitHub Repository

To support collaboration and continuous deployment, we created a GitHub repository.

GitHub enabled us to:

- Collaborate as a team.
- Track project changes.
- Manage version control.
- Maintain a central source for the application code.

Each team member contributed to the project through GitHub, making collaboration and code management more efficient.

---

## Step 7: Deploy with AWS Amplify

Instead of manually managing deployments, we used **AWS Amplify Hosting**.

The deployment process included:

1. Opening the AWS Amplify Console.
2. Selecting **Host a Web App**.
3. Connecting the GitHub repository.
4. Authorizing AWS Amplify to access the repository.
5. Selecting the project repository and deployment branch.
6. Reviewing the build configuration.
7. Deploying the application.

AWS Amplify automatically built and hosted the website.

---

## Step 8: Continuous Deployment

One of the advantages of AWS Amplify is its built-in Continuous Deployment (CI/CD).

Whenever changes are pushed to the connected GitHub repository, AWS Amplify automatically:

- Detects the new commit.
- Builds the application.
- Deploys the latest version.
- Makes the updated website available online.

This eliminates the need for manual uploads after every change.

---

## Step 9: Validate the Deployment

After deployment, we confirmed that:

- The website loaded successfully.
- Images rendered correctly.
- Stylesheets loaded properly.
- Navigation links functioned as expected.
- HTTPS was enabled automatically.
- The latest GitHub changes appeared after each deployment.

---

# 🤝 Team Collaboration

This project was completed collaboratively by **Team Delta** through the **Cloud Build With Peers** initiative.

Throughout the project we:

- Brainstormed the project concept.
- Shared responsibilities across the team.
- Collaborated using GitHub.
- Participated in sprint check-ins.
- Reviewed each other's work.
- Resolved deployment issues together.
- Documented our implementation and learning outcomes.

---

# ☁️ AWS Services Used

- AWS Identity and Access Management (IAM)
- Multi-Factor Authentication (MFA)
- AWS Amplify Hosting
- GitHub

---

# 📚 Learning Outcomes

By completing this project, Team Delta gained practical experience in:

- AWS account setup and security.
- Identity and Access Management (IAM).
- Multi-Factor Authentication (MFA).
- Static website hosting.
- GitHub version control.
- Deploying applications with AWS Amplify.
- Continuous deployment using GitHub and AWS Amplify.
- Team collaboration using Agile-inspired practices.
One recommendation

I would make one small improvement to reflect the project accurately.

Instead of saying:

Configure Static Website Hosting

I'd change the heading to:

Prepare the Static Website for Deployment

because Amplify is doing the hosting, while the website itself remains a static site. That wording is technically accurate and won't confuse reviewers into thinking you configured S3 static website hosting directly.

I think this version better reflects what your team actually did:

✅ AWS Account Setup
✅ MFA
✅ IAM
✅ Static website development
✅ GitHub collaboration
✅ AWS Amplify deployment
✅ Automatic deployments from GitHub
✅ Team-based Agile workflow

It tells the real story of your project rather than the original Builder Challenge verbatim.