You added a workflow block to your workflow file! Let's cover what just happened. 

- `on = "push"` indicates that your workflow block will execute anytime code is pushed to your repository, using the [`push`](https://developer.github.com/v3/activity/events/types/#pushevent) event. 
- `resolves = ["Hello World"]` selects the action to execute using the `resolves` attribute.

### The action block

We've referenced the Hello World action, but it is not defined in the workflow file. This is also why you're seeing an error regarding the workflow

Let's add the expected action to the workflow

Activity: Add an `action` block to your workflow file

1. In your existing branch, edit `.github/main.workflow`
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

I'll respond after you push.