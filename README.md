# bastiond

The purpose of bastiond is the following:

* A central and secure terminal for managing infrastructure using [Terraform](https://www.terraform.io/) and [Kubernetes](https://kubernetes.io/) on all major cloud providers.
* Ability to create private endpoints to triggers deployments and outgoing webhooks for delivering logs and alerts.
* Ability to create and save your state and govern access.

## How to use it:

1. Authenticate with the bastiond web terminal.
2. Create a workspace. (`bd workspace create my-awesome-app`)
3. Connect with your cloud provider(s). (`bd connect gcloud`)
4. Use `git` to pull your Kubernetes and/or Terraform files and orchestrate as usual.

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
