# Kubernetes Manifests CI

This repository contains Kubernetes manifests and CI pipeline for their validation.

## Features

- Automatic validation of Kubernetes manifests using kubeconform
- Parallel validation for multiple manifests
- Slack notifications about validation status
- Strict validation mode

## Setup

1. Create a Slack webhook:
    - Go to Slack Apps
    - Create new app
    - Enable Incoming Webhooks
    - Copy webhook URL

2. Add the Slack webhook URL to GitHub repository secrets:
    - Go to repository Settings
    - Select Secrets and variables -> Actions
    - Create new secret `SLACK_WEBHOOK` with your webhook URL

## CI Pipeline

The CI pipeline will run automatically when:
- Push to repository with changes in `k8s/` directory
- Create Pull Request with changes in `k8s/` directory

## Validation Rules

- Strict schema validation
- Parallel validation for multiple manifests
- Immediate feedback via Slack notifications