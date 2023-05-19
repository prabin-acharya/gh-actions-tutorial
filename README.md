## Hello World

```
This is a test repository for GitHub Actions.
```

This is a simple introductory workflow to help you get started with GitHub Actions.

A workflow is a configurable automated process made up of one or more jobs. You must create a workflow file to use GitHub Actions. The file is made up of one or more jobs and can be scheduled to run at specific times or events.

### Workflow syntax for GitHub Actions

```yaml
name: Hello World
on: [push]
jobs:
  build:
    name: Hello World Action
    runs-on: ubuntu-latest
    steps:
      - name: Print a greeting
        run: echo "Hello, world"
```

### This workflow contains a single job called "build"

A job contains a set of steps that perform an action, such as building your project, running tests, or deploying your application.

### The `runs-on` key tells the job to run on the latest version of Ubuntu

GitHub Actions provides hosted virtual environments for building, testing, and deploying your project. Each job in a workflow runs in a fresh instance of an environment, so steps in one job can't access filesystem artifacts created by previous jobs. The `runs-on` key specifies the type of machine to use for the job's virtual environment.

### The `steps` key contains a single step that prints a greeting

A step is a set of tasks performed by a job. Steps can run commands, run setup tasks, or run an action in your repository, a public repository, or an action published in a Docker registry. Not all steps run actions, but all actions run as a step. Steps can also run multiple actions.
