# Exercise 2:2 - Lights

This exercise is similar to the [previous one](/part2/exercises/1-locks) in that we will be building a new CRD and controller, but this time we will aim to model the "lights" part of the home automation system. Remember, there are 3 parts to the home automation system - "locks", "lights" and "temperature".

Once the "Light" CRD has been created and installed, users (or other systems) will be able to use the following yaml to interact with the lights system:

```
apiVersion: thegreatk8s.workshop.io/v1alpha1
kind: Light
metadata:
  name: bedroom-lamp
spec:
  brightness: 0.4
  colour: white
status:
  conditions:
  - lastTransitionTime: "2019-07-22T10:48:39Z"
    message: Successfully adjusted light
    reason: SuccessfulAdjustment
    status: "True"
    type: Ready
```
