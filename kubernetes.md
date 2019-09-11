# kubernetes

## Q: how do i set autodeploy to off?

kubectl label --overwrite namespace `my-namespace` automaticDeployment=off

