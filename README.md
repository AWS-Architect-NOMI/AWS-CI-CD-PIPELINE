# AWS-CI-CD-PIPELINE
Project 3: CI/CD Pipeline with AWS CodePipeline

Introduction

A Continuous Integration/Continuous Deployment (CI/CD) pipeline automates the software release process, ensuring rapid and reliable application updates. This project involves setting up an automated deployment pipeline using AWS CodePipeline, CodeBuild, and CodeDeploy.

Architecture Overview

AWS CodeCommit: Stores source code.

AWS CodeBuild: Builds and tests the application.

AWS CodeDeploy: Deploys the application to an EC2 instance.

Step-by-Step Implementation

Set Up CodeCommit Repository:

aws codecommit create-repository --repository-name MyRepo

Configure CodeBuild:

Define a buildspec.yml file:

version: 0.2
phases:
  install:
    runtime-versions:
      nodejs: 14
  build:
    commands:
      - echo "Building the project"
      - npm install
      - npm run build

Set Up CodePipeline:

aws codepipeline create-pipeline --name MyPipeline --role-arn execution-role

Deploy and Validate the Pipeline:

Push a code update to CodeCommit, and verify the automated build and deployment.

Achievement & Business Use Case

Achievement: Created a fully automated software release process reducing deployment errors.

Use Case: Essential for DevOps teams managing frequent software updates.

