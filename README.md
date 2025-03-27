# custom_docker_action_tutorial

custom docker action tutorial 


## Highlights

**When committing `entrypoint.sh`, ensure file stays executable**:

```
git add entrypoint.sh
git update-index --chmod=+x entrypoint.sh
```

Optionally, double-check:

```
git ls-files --stage entrypoint.sh
```

**When committing the rest**:

```
git add action.yml entrypoint.sh Dockerfile README.md
git commit -m "My first action is ready"
git tag -a -m "My first action release" v1
git push --follow-tags
```


## Inputs

`who-to-greet`: **Required** The name of the person to greet. Default `"World"`.


## Outputs

`time`: The time we greeted you.

## Example usage

### If published

```
uses: actions/hello-world-docker-action@v2
with:
  who-to-greet: 'Mona the Octocat'
```

### If unpublished action

```
steps:  
  - uses: <username>/<repo-name>@<branch-name>
    with:
      # input params if there is any
```

## Reference

Based on https://docs.github.com/en/actions/sharing-automations/creating-actions/creating-a-docker-container-action#testing-out-your-action-in-a-workflow

### More detail

action.yml: https://docs.github.com/en/actions/sharing-automations/creating-actions/metadata-syntax-for-github-actions

Dockerfile: https://docs.github.com/en/actions/sharing-automations/creating-actions/dockerfile-support-for-github-actions

entrypoint.sh:
- https://docs.github.com/en/actions/writing-workflows/choosing-what-your-workflow-does/workflow-commands-for-github-actions#setting-an-output-parameter
- https://docs.github.com/en/actions/sharing-automations/creating-actions/setting-exit-codes-for-actions

versioning the action: https://docs.github.com/en/actions/sharing-automations/creating-actions/about-custom-actions#using-release-management-for-actions
