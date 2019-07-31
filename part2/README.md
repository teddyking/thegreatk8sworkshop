# Part 2: Control Yourselves

## About

In the [previous session](/part1) we took a look at the kubernetes API and the
underlying components that make it tick - Resources and Controllers. We also
saw how to interact with the API by declaring some desired state in a .yml file
(e.g. my-redis-pod.yml) and then using `kubectl apply -f` to send our desired
state to the API.

This is all well and good when interacting with the default resource types
(`Deployment`, `Pod`, `Service`, etc), but where things start to get really
exciting is with our own custom resources!

In this part of the workshop we're going to get hands on with Custom Resource
Definitions (CRDs) and custom controllers.

## Learnings and Outcomes

1. An understanding of how to extend the core kubernetes API via CRDs and
   custom controllers
1. How to build, test and run your very own CRD and controller
