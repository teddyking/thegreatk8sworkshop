# Exercise 2:1 - Locks

This exercise is the first in a series of exercises that will see us through building a completely new system on top of the kubernetes API. The system we'll be building is that of a home automation system.

There are 3 parts to the home automation system - "locks", "lights" and "temperature".

We'll begin by modelling the "locks" part of the system by creating a "Lock" CRD and custom controller. Once the CRD has been created and installed, users (or other systems) will be able to use the following yaml to interact with the locks system:

```
apiVersion: thegreatk8s.workshop.io/v1alpha1
kind: Lock
metadata:
  name: front-door
spec:
  uniqueAddress: front-door.my-house.london
  lock: true
status:
  conditions:
  - lastTransitionTime: "2019-07-22T10:48:39Z"
    message: Successfully locked the door
    reason: SuccessfulLock
    status: "True"
    type: Ready
```
