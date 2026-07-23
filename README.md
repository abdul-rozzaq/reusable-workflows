# GitHub Action Templates

This repository contains a reusable GitHub Actions workflow template for building and pushing a Docker image to a container registry, with optional Telegram notifications.

## Included template

- Workflow template: .github/workflow-templates/docker-build-push.yml
- Template metadata: .github/workflow-templates/docker-build-push.properties.json

## Prerequisites

Set these repository variables before using the workflow:

- DOCKER_REGISTRY_NAME
- DOCKER_REGISTRY_USERNAME

Set these repository secrets:

- DOCKER_REGISTRY_TOKEN
- TELEGRAM_CHAT_ID
- TELEGRAM_BOT_TOKEN

## How to use it

1. Open your GitHub repository.
2. Go to Actions and choose New workflow.
3. Select the Docker Build and Push template.
4. Review the workflow, commit it, and run it.

## What the workflow does

- Checks out your code
- Logs in to your container registry
- Builds and pushes a Docker image
- Caches build layers with GitHub Actions cache
- Sends a Telegram message when the required secrets are available

## Notes

- The workflow runs on pushes to the main branch and can also be triggered manually.
- If your project uses a different Dockerfile path or build context, update the workflow accordingly.
