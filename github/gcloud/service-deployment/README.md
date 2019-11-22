# Google Cloud Service deployment

## How to start

if you need more context how to configure and use Github workflows you can look at [automating your workflow with actions](https://help.github.com/en/actions/automating-your-workflow-with-github-actions/configuring-a-workflow)

## Google auth

Google auth is required for all deployment.

Requirements:

- Google Cloud Platform project
- GCP Service Account with write access to GCR and GKE for this project
- GCP Service Account credentials stored as a JSON key. Base64 encode the JSON key and paste the entire blob as a secret (Repository Settings --> Secrets) named GKE_KEY.
- Also add Secrets for GKE_PROJECT and GKE_EMAIL. Those can be found in the raw key JSON above.

## Build and push service to Google registry

Pre-requirements are described in _Google auth_ section.

When you want leverage into your service image build and push to registry. This configuration is for you `./.github/workflows/build-and-push-image.yml`
