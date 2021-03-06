# SPA Deploy Codebuild

![Build Status](https://github.com/ryands17/spa-deploy-cdk/workflows/CI/badge.svg)

This is an [aws-cdk](https://aws.amazon.com/cdk/) project where you can deploy any SPA (React, Angular, Vue, etc.) via Codebuild on S3 and served via Cloudfront.

Link to the tutorial that I've written: https://dev.to/ryands17/deploying-a-spa-using-aws-cdk-typescript-4ibf

**_Note_**: This configuration is for GitHub only. For Bitbucket, you can edit the source accordingly.

**Prerequisites**

- Setup your access and secret keys via the [aws-cli](https://aws.amazon.com/cli/) and with the profile name of your choice (the default profile is named `default`). The credentials generated should have access to creation of all resources mentioned else it won't work.

**Steps**

1. Rename the `.example.env` file to `.env` and replace all the values with predefined values for your stack.

**_Note_**: All the variables are mandatory! Without that, the stack wouldn't work.

2. Run `yarn` (recommended) or `npm install`

3. Run `yarn deploy --profile profileName` or `npm run deploy -- --profile profileName` to deploy the stack to your specified region. You can skip providing the profile name if it is `default`.

4. You can start the build from the console in `Codebuild` and view your website on the Cloudfront provided URL!

The `cdk.json` file tells the CDK Toolkit how to execute your app.

## Commands

- `yarn build` compile typescript to js
- `yarn deploy` deploy this stack to your AWS account/region specified in the `.env`
- `yarn watch` watch for changes and compile
- `yarn test` perform the jest unit tests
- `cdk diff` compare deployed stack with current state
- `cdk synth` emits the synthesized CloudFormation template
