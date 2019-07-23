# Exercise 2:1 - Coffee

In this exercise we will use
[kubebuilder](https://github.com/kubernetes-sigs/kubebuilder) to create a CRD
with a corresponding custom controller. And the CRD we're going to create is
one of kind `Coffee`. Here's an example of what that might look like:

```
apiVersion: thegreatk8s.workshop.io/v1alpha1
kind: Coffee
metadata:
  name: my-coffee
spec:
  beans: hermanos-columbian-roast
  strength: 0.8
  volume: 35ml
status:
  conditions:
  - lastTransitionTime: "2019-07-22T10:48:39Z"
    message: Successfully brewed coffee
    reason: SuccessfulBrew
    status: "True"
    type: Ready
```
