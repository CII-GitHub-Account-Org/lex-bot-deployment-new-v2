# Lex Bot Deployment

This project deploys an Amazon Lex bot using GitHub Actions and the Serverless Framework.

## Prerequisites

- An AWS account
- A GitHub account
- Node.js and npm installed on your local machine

## Setup

1. Clone this repository to your local machine.

2. Install the dependencies by running `npm install` in the project root directory.

3. Configure your AWS credentials in the Serverless Framework. Follow the instructions in the [Serverless Framework documentation](https://www.serverless.com/framework/docs/providers/aws/guide/credentials/).

4. Set up a GitHub OpenId Connect IAM Role to interact with your AWS account. Follow the instructions in the [GitHub documentation](https://docs.github.com/en/actions/deployment/security-hardening-your-deployments/about-security-hardening-with-openid-connect).

5. Set the `AWS_ACCESS_KEY_ID`, `AWS_SECRET_ACCESS_KEY`, and `AWS_SESSION_TOKEN` as secrets in your GitHub repository. These are used by the GitHub Actions workflow to authenticate with AWS.

## Deployment

The Lex bot is automatically deployed whenever you push to the repository. The deployment is handled by a GitHub Actions workflow, which runs the `npx serverless deploy` command.

You can monitor the progress of the deployment in the Actions tab of your GitHub repository.

## Bot Definition

The definition of the Lex bot is located in the `src/bot-definition.json` file. You can modify this file to customize the bot.

## Troubleshooting

If the deployment fails, check the logs in the Actions tab of your GitHub repository. If you need further assistance, refer to the [Serverless Framework documentation](https://www.serverless.com/framework/docs/) and the [GitHub Actions documentation](https://docs.github.com/en/actions).