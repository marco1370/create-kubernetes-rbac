## Create Kubernetes Service / User Account restricted to one Namespace 

## How can I create a user and restrict user to access only one namespace in Kubernetes?. Kubernetes gives you a way to regulate access to Kubernetes clusters and resources based on the roles of individual users through a feature called Role-based access control (RBAC)
**

  ```
Role: A role contains rules that represent a set of permissions. A role is used to grant access to resources within a namespace.
RoleBinding: A role binding is used to grant the permissions defined in a role to a user or set of users. It holds a list of subjects (users, groups, or service accounts), and a reference to the role being granted
Service Account: Account meant for for processes, which run in pods
```


To achieve a complete isolation in Kubernetes, we’ll use the concepts on namespaces and role based access control. The idea behind service accounts is based on the principle of least privilege. An account is created for specific tasks.

 
## Create and Limit Service account to a namespace in Kubernetes

```
Step 1: Create a namespace
Step 2: Create a Service Account
Step 3: Create a Role
Step 4: Bind the role to a user
Step 5: Creating kubectl configuration

```


## Request a token to authenticate to the kube-apiserver as the service account "myapp-demozarin-v4" in the current namespace

```
kubectl create token zarinpal-v4-demo-user    --duration 100000  -n zarinpal-v4-demo



  # Request a token with a custom expiration


  kubectl create token myazarinpal-v4-demo-user  --duration 10m
```
