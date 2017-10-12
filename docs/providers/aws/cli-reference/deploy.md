<!--
title: Serverless Framework Commands - AWS Lambda - Deploy
menuText: deploy
menuOrder: 5
description: Deploy your service to the specified provider
layout: Doc
-->

<!-- DOCS-SITE-LINK:START automatically generated  -->
### [Read this on the main serverless docs site](https://www.serverless.com/framework/docs/providers/aws/cli-reference/deploy)
<!-- DOCS-SITE-LINK:END -->

# AWS - deploy

The `sls deploy` command deploys your entire service via CloudFormation.  Run this command when you have made infrastructure changes (i.e., you edited `serverless.yml`).  Use `serverless deploy function -f myFunction` when you have made code changes and you want to quickly upload your updated code to AWS Lambda or just change function configuration.

```bash
serverless deploy
```

## Options
- `--stage` or `-s` The stage in your service that you want to deploy to.
- `--region` or `-r` The region in that stage that you want to deploy to.
- `--package` or `-p` path to a pre-packaged directory and skip packaging step.
- `--verbose` or `-v` Shows all stack events during deployment, and display any Stack Output.
- `--function` or `-f` Invoke `deploy function` (see above). Convenience shortcut - cannot be used with `--package`.

## Artifacts

After the `serverless deploy` command runs, the framework runs `serverless package` in the background first then deploys the generated package.

## Examples

### Deployment without stage and region options

```bash
serverless deploy
```

This is the simplest deployment usage possible. With this command Serverless will deploy your service to the defined
provider in the default stage (`dev`) to the default region (`us-east-1`).

### Deployment with stage and region options

```bash
serverless deploy --stage production --region eu-central-1
```

With this example we've defined that we want our service to be deployed to the `production` stage in the region
`eu-central-1`.

### Deployment from a pre-packaged directory

```bash
serverless deploy --package /path/to/package/directory
```

With this example, the packaging step will be skipped and the framework will start deploying the package from the `/path/to/package/directory` directory.
