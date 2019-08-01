# Exercise 3:1 - Room

In this exercise we'll be introducing one final CRD - "Room". The Room CRD will allow users of the home automation system to declare a desired state for an entire room - including all the locks, lights and temperature.

Once the "Room" CRD has been created and installed, users (or other systems) will be able to use the following yaml to interact with the entire home automation system:

```
apiVersion: thegreatk8s.workshop.io/v1alpha1
kind: Room
metadata:
  name: kitchen
spec:
  door: locked
  temperature: 20.0
  lights:
  - name: main
    brightness: 0.8
  - name: table
    brightness: 0.3
status:
  conditions:
  - lastTransitionTime: "2019-07-22T10:48:39Z"
    message: Successfully set room
    reason: RoomReady
    status: "True"
    type: Ready
```
