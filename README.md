# ⚡️ serverless Dart for AWS Lambda template

A sample template for bootstrapping [Dart Runtime for AWS Lambda](https://github.com/awslabs/aws-lambda-dart-runtime) applications with ⚡ serverless framework ⚡.

## 📦 Install

Install the [serverless framework](https://www.serverless.com/framework/docs/getting-started/) CLI.

Run the following command in your terminal.

```bash
$ npx serverless install \
  --url https://github.com/katallaxie/serverless-aws-dart \
  --name hello
```

This will download the source of a sample Dart application and unpack it as a new service named
"hello" in a directory called "hello" 👋.

## 🛵 Deployment

This template includes an example [GitHub actions](https://github.com/features/actions) [configuration file](.github/workflows/main.yml) which can unlock a virtuous cycle of continuous integration and deployment
( i.e all tests are run on prs and every push to master results in a deployment).

GitHub actions is managed simply by the presence of a file checked into your repository. To set up GitHub Actions to deploy to AWS you'll need to do a few things

Firstly, version control your source. [Github](https://github.com/) is free for opensource.

```bash
$ git init
$ git remote add origin git@github.com:{username}/hello.git
```

Store a `AWS_ACCESS_KEY_ID` `AWS_SECRET_ACCESS_KEY` used for aws deployment in your repositories secrets https://github.com/{username}/hello/settings/secrets

Add your changes to git and push them to GitHub.

Finally, open https://github.com/{username}/hello/actions in your browser and grab a bucket of popcorn 🍿.

## 👴 retiring

Good code should be easily replaceable. Good code should also be easily disposable. Retiring applications should be as easy as creating and deploying them them. The dual of `serverless deploy` is `serverless remove`. Use this for retiring services and cleaning up resources.

```bash
$ npx serverless remove
```

## ℹ️  additional information

* See the [serverless-dart plugin's documentation](https://github.com/katallaxie/serverless-dart) for more information on plugin usage.

* See the [Dart Runtime for AWS Lambda](https://github.com/awslabs/aws-lambda-dart-runtime) for more information on writing Dart Lambda functions
