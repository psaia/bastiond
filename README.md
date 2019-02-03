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

```shell
$ bd workspace create todo-app
todo-app created.
$ bd connect aws
$ bd connect gcloud
$ terraform apply
$ kubectl apply -f my-app.yaml
```
