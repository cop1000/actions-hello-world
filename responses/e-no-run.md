The workflow didn't run.

Here's some possible reasons why:
- files aren't in proper directories
- your script isn't executable

### Troubleshooting steps

Check out the [action's output]({{ url }}). You can also access this information by going to the [Actions tab]({{ repo }}/actions).

You can also use the following to help you troubleshoot:
<details><summary>For <code>./action-a/entrypoint.sh</code></summary>

| Problem                                                      | Solution                                                                                                                                                                                          |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `entrypoint.sh` isn't executable                             | In your shell, run `chmod +x action-a/entrypoint.sh` on this branch and push it up to GitHub.                                                                                                     |
| The file isn't called `entrypoint.sh` (case sensitive)       | Rename the file using the [UI](https://help.github.com/articles/renaming-a-file/) or [your CLI](https://help.github.com/articles/renaming-a-file-using-the-command-line/)                         |
| The directory `action-a` doesn't exist.                      | [Create the `action-a` folder](https://help.github.com/articles/creating-new-files/) and [move `entrypoint.sh`](https://help.github.com/articles/moving-a-file-to-a-new-location/) to `action-a`. |
| The `entrypoint.sh` file isn't inside the `action-a` folder. | [Move `entrypoint.sh`](https://help.github.com/articles/moving-a-file-to-a-new-location/) to `action-a`.                                                                                          |
</details>

<details><summary>For <code>./action-a/Dockerfile</code></summary>

| Problem                                              | Solution                                                                                                                                                                                           |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| The file isn't called `Dockerfile` (case sensitive)  | Rename the file using the [UI](https://help.github.com/articles/renaming-a-file/) or [your CLI](https://help.github.com/articles/renaming-a-file-using-the-command-line/)                          |
| The directory `action-a` doesn't exist.              | [Create the `action-a` folder](https://help.github.com/articles/creating-new-files/) and [move the `Dockerfile`](https://help.github.com/articles/moving-a-file-to-a-new-location/) to `action-a`. |
| The `Dockerfile` isn't inside the `action-a` folder. | [Move the `Dockerfile`](https://help.github.com/articles/moving-a-file-to-a-new-location/) to `action-a`.                                                                                          |
</details>

<details><summary>For <code>./.github/main.workflow</code></summary>

| Problem                                                     | Solution                                                                                                                                                                                        |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| There's some problem with your syntax in `main.workflow`.   | Copy and paste the code exactly as is shown in this PR (check for extra spaces, symbols) or see if an error appears in the action logs.                                                         |
| The file isn't called `main.workflow` (case sensitive)      | Rename the file using the [UI](https://help.github.com/articles/renaming-a-file/) or [your CLI](https://help.github.com/articles/renaming-a-file-using-the-command-line/)                       |
| The directory `.github` doesn't exist.                      | [Create the `.github` folder](https://help.github.com/articles/creating-new-files/) and [move `main.workflow`](https://help.github.com/articles/moving-a-file-to-a-new-location/) to `.github`. |
| The `main.workflow` file isn't inside the `.github` folder. | [Move `main.workflow`](https://help.github.com/articles/moving-a-file-to-a-new-location/) to `.github`.                                                                                         |
</details>


 Next time you push, your action will try to run. I'll respond when that occurs. 