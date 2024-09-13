# My Static Website: S3 Hosting with GitHub CI/CD

This repository contains the source code for my personal website, which is hosted as a static website on Amazon S3. I've implemented a CI/CD pipeline using GitHub Actions to automate the deployment process.

## Architecture Overview

- **Hosting**: Amazon S3 Static Website Hosting
- **Version Control**: Git (GitHub)
- **CI/CD**: GitHub Actions

## How It Works

1. **S3 Static Website Hosting**: 
   - The website content is stored in an S3 bucket configured for static website hosting.
   - This provides a scalable, reliable, and low-cost way to host static content.

2. **GitHub Repository**:
   - All website source files (HTML, CSS, JavaScript, images, etc.) are version-controlled in this GitHub repository.

3. **CI/CD Pipeline with GitHub Actions**:
   - Whenever changes are pushed to the `main` branch, a GitHub Actions workflow is triggered.
   - The workflow automates the following steps:
     a. Builds the website (if necessary, e.g., for static site generators)
     b. Runs any tests
     c. Syncs the built files to the S3 bucket

## Setup and Configuration

1. **S3 Bucket Setup**:
   - Created an S3 bucket and enabled static website hosting
   - Configured bucket policy for public read access

2. **GitHub Repository**:
   - Initialized a new repository
   - Added all website source files

3. **GitHub Actions Workflow**:
   - Created a `.github/workflows/frontend-cicd.yml` file to define the CI/CD pipeline
   - Configured AWS credentials as GitHub secrets for secure access

4. **DNS Configuration** (if applicable):
   - Set up a custom domain to point to the S3 website endpoint

## Deployment

With this setup, deploying changes to the website is as simple as pushing to the `main` branch. The GitHub Actions workflow takes care of building and deploying the site automatically.

## Benefits of This Approach

- **Version Control**: Full history of all changes to the website
- **Automated Deployments**: Reduces manual errors and saves time
- **Scalability**: S3 can handle any amount of traffic
- **Cost-Effective**: Pay only for the storage and bandwidth you use