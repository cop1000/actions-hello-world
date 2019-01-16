# Welcome 

This course is a companion to the Developer Guide [Creating a new workflow](https://developer.github.com/actions/creating-workflows/creating-a-new-workflow/). We'll provide some context in issues and pull requests, but head on over to the docs for the full instructions.

There are two components to using GitHub Actions that we'll cover:
- the action itself
- a workflow that utilizes the action

## Step 1: Add a Dockerfile

Every GitHub Action runs in a Docker container and requires a Dockerfile. Let's add it now. 

### :keyboard: Activity: Create a Dockerfile and open a pull request

1. Create a branch.
1. In your new branch, create a directory: `action-a`.
1. In your new directory, create a file titled `Dockerfile`.
1. Fill the Dockerfile with the content below:
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
1. Stage and commit your file.
1. Push the `Dockerfile` up to GitHub.
1. Open a pull request with your new branch against `master`.

<hr>
<h3 align="center">I'll respond in your new pull request with next steps.</h3>
