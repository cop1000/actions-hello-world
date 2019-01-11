Your script was added.

We'll now define a workflow that utilizes your GitHub Action.

There are two blocks in our workflow file:
- workflow
- action

### Workflow block

The `on` attribute identifies the event.
The `resolves` attribute points to an action block.

### Action block

TBD

Let's add the templated workflow:

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