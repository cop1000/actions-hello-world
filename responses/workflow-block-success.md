Nice work! :tada: You added a workflow block to your workflow file! Let's cover what just happened. 

- `on = "push"` indicates that your workflow block will execute anytime code is pushed to your repository, using the [`push`](https://developer.github.com/v3/activity/events/types/#pushevent) event. 
- `resolves = ["Hello World"]` selects the action to execute using the `resolves` attribute.

### The action block

We've referenced the Hello World action, but it is not defined in the workflow file. This is also why you're seeing an error regarding the workflow.

## Step 4: Add a `action` block to your workflow file

Let's add the expected action to the workflow.

### :keyboard: Activity: Add an `action` block to your workflow file and commit it to your branch

1. In your existing branch, edit `.github/main.workflow`.
1. Append the following content to the file:
    ```hcl
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

<hr>
<h3 align="center">I'll respond below with your next step.</h3>
