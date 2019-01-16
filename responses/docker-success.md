Hey! You submitted a Dockerfile! :tada: You'll notice at the end of the Dockerfile, we refer to an entrypoint script: 

```Dockerfile
ENTRYPOINT ["/entrypoint.sh"]
```
## Step 3: Add an entrypoint script

An entrypoint script must exist in our repository. Let's add it. 

### :keyboard: Activity: Add an entrypoint script and commit it to your pull request

1. In your existing branch and folder (`./action-a/`), create a file titled `entrypoint.sh`.
1. Add the following content to your script:
    ```shell
    #!/bin/sh -l

    sh -c "echo $*"
    ```
1. Ensure the script is executable:
    ```shell
    chmod +x action-a/entrypoint.sh
    ```
1. Stage and commit your script.
1. Push it up to GitHub. 

<hr>
<h3 align="center">I'll respond below with your next step.</h3>
