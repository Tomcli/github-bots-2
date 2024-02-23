# Welcome to the github bots repo
This code repository (or "repo") is designed to host all the tools for running github bots

# Deploy prow with free tier github actions

Open Labrador organization already created a prow github action template. To use it, please proceed with the following steps:
1. Install the `Open Labrador Github Actions Prow` github action.

  <img width="977" alt="Screenshot 2024-02-22 at 3 58 47 PM" src="https://github.com/open-labrador/github-bots/assets/10889249/f85d4393-d041-4435-9c42-4798991751c1">
  <break></break>
  <img width="633" alt="Screenshot 2024-02-22 at 3 59 01 PM" src="https://github.com/open-labrador/github-bots/assets/10889249/a7f2d85e-2eb0-43f4-93bb-e23840c74087">
  <break></break>
  <img width="402" alt="Screenshot 2024-02-22 at 3 59 13 PM" src="https://github.com/open-labrador/github-bots/assets/10889249/c067faa6-6b80-45fe-b171-721e4a07664a">

2. Create an `OWNERS` file in the root directory. Here is the [Kubernetes OWNERS file format](https://www.kubernetes.dev/docs/guide/owners/).

3. Create a `labels.yml` file inside the `.github` directory. The labels.yml is a list of labels that the bots are allowed to use. Here is the [example for the labels.yml file](/.github/labels.yml).

# Back Up Plan
To deploy the full Prow bot on Kubernetes, please visit the [prow](/prow) directory.
