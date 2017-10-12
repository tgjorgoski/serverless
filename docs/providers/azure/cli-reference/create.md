<!--
title: Serverless Framework Commands - Azure Functions - Create
menuText: create
menuOrder: 1
description: Creates a new Service in your current working directory
layout: Doc
-->

<!-- DOCS-SITE-LINK:START automatically generated  -->
### [Read this on the main serverless docs site](https://www.serverless.com/framework/docs/providers/azure/cli-reference/create)
<!-- DOCS-SITE-LINK:END -->

# Azure - Create

Creates a new service in the current working directory based on the specified
template.

**Create service in current working directory:**

```bash
serverless create --template azure-nodejs
```

**Create service in new folder:**

```bash
serverless create --template azure-nodejs --path myService
```

## Options
- `--template` or `-t` The name of one of the available templates. **Required**.
- `--path` or `-p` The path where the service should be created.
- `--name` or `-n` the name of the service in `serverless.yml`.

## Provided lifecycle events
- `create:create`

## Available Templates

To see a list of available templates run `serverless create --help`

Most commonly used templates:

- azure-nodejs

## Examples

### Creating a new service

```bash
serverless create --template azure-nodejs --name my-special-service
```

This example will generate scaffolding for a service with `Azure` as a provider
and `nodejs` as runtime. The scaffolding will be generated in the current working
directory.

### Creating a named service in a (new) directory

```bash
serverless create --template azure-nodejs --path my-new-service
```

This example will generate scaffolding for a service with `Azure` as a provider
and `nodejs` as runtime. The scaffolding will be generated in the `my-new-
service` directory. This directory will be created if not present. Otherwise
Serverless will use the already present directory.

Additionally Serverless will rename the service according to the path you
provide. In this example the service will be renamed to `my-new-service`.
