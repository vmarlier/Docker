# Terraform-scw-kctl
> General description:
This image will be used to deploy kubernetes infrastructure and application on scaleway cloud.

### Table of contents
* [General Informations](#general-info)
* [Releases](#releases)
* [How to Commit](#how-to-commit)

### General Informations
This image is based on alpine linux and include terraform, kubectl and scw (scaleway cli).

### Releases
| Release | Terraform | Kubectl | Scaleway CLI | Changelog |
| ------ | ------ | ------ | ------ | ------ |
| v0.1 | 1.14 | 1.20 | 2.2.3 | |

### How to commit
Here is a guide to make clean commit in this project.
```sh
$ git commit -m "[STATUS] Here is the message"
```
**Status**
* ADD : When you add a new file or a new functionality
* UPDATE : When you modify a functionality
* DONE : When you finish a task/function
* WIP : When your work still in progress
* BUG : In case you create a Bug
* FIXED : When you fixed a bug

**Examples**
```
$ git commit -m "[ADD] newFunction()"
$ git commit -m "[DONE] Lambda x"
$ git commit -m "[WIP] missing return statement newFunction()"
$ git commit -m "[BUG] callLambda() don't work"
$ git commit -m "[FIXED] callLambda() don't work: API gateway did not allowed usage of GET method"
```
You can combine status
```
git commit -m "[WIP/BUG] still working on callLambda() bug"
```
