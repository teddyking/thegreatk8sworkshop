# Part 1.1: An Understanding of Why the Kubernetes API Is So Good

## About

There are a number of qualities that make the kubernetes API so attractive.

The first is that it is a declarative API; when interacting with the API you
tell it _what_ you want, not _how_ to do it. For example, "I want 3 nginx pods",
rather than, "Create 3 nginx pods". Declarative APIs are desirable for a number
of reasons, particularly with regards to the design of highly distributed
systems (such as kubernetes). They ...

The second great quality of the API is that it is "level-based" as opposed to
"edge-based". In short, the benefit of this is that the system is much more
resilient in the face of disruption. There is an excellent article, [Level
Triggering and Reconciliation in
Kubernetes](https://hackernoon.com/level-triggering-and-reconciliation-in-kubernetes-1f17fe30333d),
which goes into more detail about this, and I highly recommend giving it a read.

Separation of state
Transparent

## Further Reading

* Declarative vs imperative linkys
* Distributed systems declarative etc.

## Exercise

Let's put this into action
