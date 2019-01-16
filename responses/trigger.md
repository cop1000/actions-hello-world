Nice! :sparkles:You added the action block! Let's go over it.

- `uses = "./action-a"`: the action block uses `action-a` by referencing the path to the action's directory, relative to your `hello-world-actions` repository.
- `env = { ... }`: uses the `env` action attribute to create an environment variable that will be available to your action in the runtime environment. In this case, the environment variable is `MY_NAME`, and it is currently initialized to `"Mona"`.
-  `args = "\"Hello world, I'm $MY_NAME!\""`: finally, you'll pass a string to the action in the `args` attribute. The `args` you pass are appended to the `echo` command in `entrypoint.sh` and run in a command shell. This allows you to use environment variables in the `args` attribute. See "[`ENTRYPOINT`](https://developer.github.com/actions/creating-github-actions/creating-a-docker-container/#entrypoint)" for more about how the `entrypoint.sh` file works.

### Your action is about to be triggered!

Your repository now contains everything it needs for the action to be defined (in the `./action-a/` folder) and everything it needs to be triggered (in the `./github/main.workflow` file).

The action will run anytime you push code to your repository. Since you just pushed, the action will be triggered. Let's wait for the workflow to be triggered. This might take a few minutes since it's the first time it runs on this repo. 

### Seeing your Action in action

You can see the action status reported below, or you can click the "Actions" tab in your repository. From there you will see the actions that have run, and you can click on the action's "Log" link to view details.

![View an action's log](https://developer.github.com/assets/images/actions-view-log.png)

## Step 5: Trigger the workflow

### :keyboard: Activity: See your action trigger the workflow

1. You've done the work, not sit back and see your action trigger the workflow!

<hr>
<h3 align="center">I'll respond below when I detect your action has run and reported a status.</h3>

> _Sometimes I respond too fast for the page to update! If you perform an expected action and don't see a response, wait a few seconds and refresh the page for your next steps._
