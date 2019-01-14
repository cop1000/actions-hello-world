Welcome! This course is a companion to the Developer Guide [Creating a new workflow](https://developer.github.com/actions/creating-workflows/creating-a-new-workflow/). We'll provide some context in issues and pull requests, but head on over to the docs for the full instructions.

This example manually creates a workflow and an action, rather than using the visual editor. The workflow in this example uses the action created in the "[Hello world action example](https://developer.github.com/actions/creating-github-actions/creating-a-new-action/#hello-world-action-example)" to write values to standard output (`stdout`).

The action writes any values passed in the `args` [action attribute](https://developer.github.com/actions/creating-workflows/workflow-configuration-options#actions-attributes) to `stdout`.

Here's an overview of the file hierarchy you'll use:

```
|-- hello-world-actions (repository)
|   |__ .github
|       |__ main.workflow
|   |__ action-a
|       │__  Dockerfile
|       |__  entrypoint.sh  
|
```

Activity: Create a Dockerfile

1. Create a branch.
1. In your new branch, create a directory: `action-a`
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
1. Push the file up to GitHub.
1. Open a pull request with your new branch against `master`.

I'll respond in your new pull request when you open it.