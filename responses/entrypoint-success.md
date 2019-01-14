The entrypoint script was added!

We'll now define a workflow that utilizes your GitHub Action.

You'll need one [workflow block](https://developer.github.com/actions/creating-workflows/workflow-configuration-options/#workflow-blocks) and one [action block](https://developer.github.com/actions/creating-workflows/workflow-configuration-options/#action-blocks) for this example.

Your workflow block will execute anytime code is pushed to your repository, using the [`push`](https://developer.github.com/v3/activity/events/types/#pushevent) event. The workflow selects the action to execute using the `resolves` attribute.

The action block uses `action-a` by referencing the path to the action's directory, relative to your `hello-world-actions` repository.

Use the `env` action attribute to create an environment variable that will be available to your action in the runtime environment. Finally, you'll pass a string to the action in the `args` attribute. The `args` you pass are appended to the `echo` command in `entrypoint.sh` and run in a command shell. This allows you to use environment variables in the `args` attribute. See "[`ENTRYPOINT`](https://developer.github.com/actions/creating-github-actions/creating-a-docker-container/#entrypoint)" for more about how the `entrypoint.sh` file works.

Activity: Define a workflow 

1. In your existing branch, create a folder titled `.github`.
1. In the new folder, create a file titled: `main.workflow`.
1. Add the following content to your workflow:
    ```hcl
    workflow "New workflow" {
      on = "push"
      resolves = ["Hello World"]
    }

    action "Hello World" {
      uses = "./action-a"
      env = {
        MY_NAME = "Mona"
      }
      args = "\"Hello world, I'm $MY_NAME!\""
    }
    ```
1. Stage and commit your workflow.
1. Push it up to GitHub. 

I'll respond after you push.