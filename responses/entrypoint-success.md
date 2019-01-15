The entrypoint script was added!

We'll now define a workflow that utilizes your GitHub Action.

You'll need one [workflow block](https://developer.github.com/actions/creating-workflows/workflow-configuration-options/#workflow-blocks) and one [action block](https://developer.github.com/actions/creating-workflows/workflow-configuration-options/#action-blocks) for this example.

First, we'll add the workflow block. We'll add the action block in a later step. 

### The workflow block

Your workflow block will execute anytime code is pushed to your repository, using the [`push`](https://developer.github.com/v3/activity/events/types/#pushevent) event. The workflow selects the action to execute using the `resolves` attribute.

Activity: Add a `workflow` block to your workflow file

1. In your existing branch, create a folder titled `.github`.
1. In the new folder, create a file titled: `main.workflow`.
1. Add the following content to your workflow:
    ```hcl
    workflow "New workflow" {
      on = "push"
      resolves = ["Hello World"]
    }
    ```
1. Stage and commit your workflow.
1. Push it up to GitHub. 

<details><summary>Trouble pushing?</summary>

The `main.workflow` file cannot edited using an integration. Try editing the file using the web interface, or your command line.

It is possible that you are using an integration (like GitHub Desktop or any other tool that authenticates as you and pushes on your behalf) if you receive a message like the one below:

```shell
To https://github.com/your-username/your-repo.git
 ! [remote rejected] your-branch -> your-branch (refusing to allow an integration to update main.workflow)
error: failed to push some refs to 'https://github.com/your-username/your-repo.git'
```
</details>
<br />
I'll respond after you push.