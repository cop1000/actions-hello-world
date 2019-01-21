Welcome! This is a companion course to the Developer Guide: [Creating a new workflow](https://developer.github.com/actions/creating-workflows/creating-a-new-workflow/). For the most complete information, see the[documentation](https://developer.github.com/actions/).


### Actions and Workflows
There are two components to using GitHub Actions that we'll cover:
- the **action** itself
- a **workflow** that uses the action

A workflow can contain many actions, but each action has its own purpose. So, we'll put the files relating to the action in their own directory.

## Step 1: Creating a `Dockerfile`

Every GitHub Action runs in a Docker container and requires a `Dockerfile`. Let's add it now. We won't discuss what each line means in detail, but the important thing to know is that the action will be executed in an environment defined by this file.

### :keyboard: Activity: Create a `Dockerfile`

1. Create a new branch
  - _Branches should be named intentionally, so a good name for this branch could be `first-action`_
1. On the new branch, create a directory: `action-a`
1. In the `action-a` directory, create a file titled `Dockerfile`
1. Fill the `Dockerfile` with the content below:
    ```Dockerfile
    FROM debian:9.5-slim

    LABEL "com.github.actions.name"="Hello World"
    LABEL "com.github.actions.description"="Write arguments to the standard output"
    LABEL "com.github.actions.icon"="mic"
    LABEL "com.github.actions.color"="purple"

    LABEL "repository"="http://github.com/octocat/hello-world"
    LABEL "homepage"="http://github.com/actions"
    LABEL "maintainer"="Octocat <octocat@github.com>"

    ADD entrypoint.sh /entrypoint.sh
    ENTRYPOINT ["/entrypoint.sh"]
    ```
1. Stage and commit your file
1. Open a pull request with your new branch against `master`
- If you're working locally, you will first need to push the branch to GitHub

<hr>
<h3 align="center">I'll respond in your new pull request.</h3>
