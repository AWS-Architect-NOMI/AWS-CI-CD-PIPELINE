# AWS-CI-CD-PIPELINE
Introduction

A Continuous Integration/Continuous Deployment (CI/CD) pipeline automates code deployment.

Architecture Overview

AWS CodeCommit: Stores source code.

AWS CodeBuild: Builds the application.

AWS CodeDeploy: Deploys the application.

Step-by-Step Implementation

Set Up CodeCommit Repository:

aws codecommit create-repository --repository-name MyRepo

Configure CodeBuild:

Define a buildspec.yml file:

version: 0.2
phases:
  build:
    commands:
      - echo "Building the project"

Set Up CodePipeline:

aws codepipeline create-pipeline --name MyPipeline --role-arn execution-role

Result

Your pipeline automates the build and deployment process.
