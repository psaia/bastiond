# bastiond

The purpose of bastiond is the following:

* A central and secure terminal for managing infrastructure using tools like [Terraform](https://www.terraform.io/) and [Kubernetes](https://kubernetes.io/) on all major cloud providers.
* Ability to create private endpoints (API) to trigger deployments and outgoing webhooks for delivering logs and alerts.
* Ability to create and save your state and govern access.

![diagram](https://i.imgur.com/PubZNMM.png)

## How to use it:

1. Authenticate with the bastiond web terminal.
2. Create a workspace. (`bd workspace create [aws|azure|gcloud]/my-awesome-app-staging`)
3. Use `git` to pull your Kubernetes and/or Terraform files or create from scratch and orchestrate as usual.

```bash
$ bd workspace create aws/todo-app
todo-app for AWS has been created.
$ bd workspace create gcloud/todo-app
todo-app for Google Cloud has been created.
$ bd workspace change aws/todo-app
You are now in the todo-app Project within AWS.
$ ... Create or checkout terraform or k8s files ...
$ terraform apply
$ kubectl apply -f my-app.yaml
```

## Web CLI Documentation

* [Workspaces](#workspaces)
* [Webhooks](#webhooks)
* [Access Management](#access-management)
* [Account Management](#account-management)

### Workspaces

A workspace in bastiond is a stateful and restricted environment that is connected to a cloud provider. Your workspace will
always be saved along with a full history log.

**List: `bd workspace list`**

List all available workspaces.

**Create: `bd workspace create [gcloud|aws|azure]/[project name]`**

Create and switch to a new cloud environment.

**Change: `bd workspace change [project name]`**

Switch to a workspace.

**Remove: `bd workspace remove [project name]`**

Permenantly remove a workspace.

### Webhooks

Webhooks allow you to create powerful automations using your Git providers, communication tools, and CI tools.

Some common use cases are:

* Create incoming webhook for CI to trigger a deployment configuration. 
* Create outgoing webhook to deliver a payload of logs after a deployment is executed.

### Access Management

You can easily share access to a workspace to anyone using bastiond.

### Account Management

Update email, password, 2FA, etc.
