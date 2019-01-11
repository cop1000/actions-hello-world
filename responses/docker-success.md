Hey! You submitted a Dockerfile! Let's add the entrypoint script.

We would normally take these Docker images and put them into Dockerhub. We can now version control and publish as part of our workflow.

If we do want to publish to Dockerhub, we can use an existing Action called Docker registry.

Now let's add the entrypoint script.

In `./action-a/entrypoint.sh`:
```shell
#!/bin/sh -l

sh -c "echo $*"
```