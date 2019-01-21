Hey! You submitted a Dockerfile! You'll notice at the end of the Dockerfile, we refer to an entrypoint script: 

```Dockerfile
ENTRYPOINT ["/entrypoint.sh"]
```

That script must exist in our repository. Let's add it. 

Activity: Add an entrypoint script

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

I'll respond in this PR when I detect the push. 