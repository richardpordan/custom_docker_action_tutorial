# custom_docker_action_tutorial

custom docker action tutorial 

## Docs

based on https://docs.github.com/en/actions/sharing-automations/creating-actions/creating-a-docker-container-action#testing-out-your-action-in-a-workflow

action.yml: https://docs.github.com/en/actions/sharing-automations/creating-actions/metadata-syntax-for-github-actions

Dockerfile: https://docs.github.com/en/actions/sharing-automations/creating-actions/dockerfile-support-for-github-actions

entrypoint.sh:
- https://docs.github.com/en/actions/writing-workflows/choosing-what-your-workflow-does/workflow-commands-for-github-actions#setting-an-output-parameter
- https://docs.github.com/en/actions/sharing-automations/creating-actions/setting-exit-codes-for-actions

versioning the action: https://docs.github.com/en/actions/sharing-automations/creating-actions/about-custom-actions#using-release-management-for-actions

## Inputs

## `who-to-greet`

**Required** The name of the person to greet. Default `"World"`.

## Outputs

## `time`

The time we greeted you.

## Example usage

uses: actions/hello-world-docker-action@v2
with:
  who-to-greet: 'Mona the Octocat'