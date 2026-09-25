-- Custom Resource Definition --

To Add additional capabilities to the kubernetes cluster, we extend API server to add those capabilities, we extend this by introducing three things :-

1. Custom Resource Definition
2. Custom Resource
3. Custom Controller

# Implementation

- We must create custom resource definition - definition that validates the custom resource is correctly configured or not.
- Then we must deploy custom controller which actually does the action part and do the job.
- Then we create custom resource -> which is validates by if this cr(custom-resource) follows that crd (custom-resource-definition).
- This is how whole process is done, this is natively followed by kubernetes under the hood where there is a -> kubernetes controller validates native resources against their definitions which are already defined in the kubernetes cluster.

- You could write a controller in most preffered way in golang (clientgo,controller runtime)
- Checkout both to acquire knowledge on how controllers are written for custom resource provisioning.
