# Part 1.1: An Understanding of Why the Kubernetes API Is So Good

## About

There are a number of qualities that make the kubernetes API so attractive.

### Declarative

The first is that it is a declarative API; when interacting with the API you
tell it _what_ you want, not _how_ to do it. For example, "I want 3 nginx pods",
rather than, "Create 3 nginx pods". Declarative APIs are desirable for a number
of reasons, particularly with regards to the design of highly distributed
systems (such as kubernetes). They ...

### Level-based

The second great quality of the API is that it is "level-based" as opposed to
"edge-based". In level-based systems, components react to the current observed
state of the world, and as such, do not need to rely on previously-observed
states in order to make decisions. In short the benefit of this is that
level-based systems are much more resilient in the face of disruption. This is
not the case with edge-based systems. The article, "[Level Triggering and
Reconciliation in
Kubernetes](https://hackernoon.com/level-triggering-and-reconciliation-in-kubernetes-1f17fe30333d)"
provides a really great overview of level-based vs edge-based systems and is
great reading on the subject.

### Separation of state

The kubernetes API separates its state into two - desired state and observed
state. Users of the API (human or machine) express a desired state and the
system continually works to make it so. As the system works it reports the
current observed state. This clear separation makes the system as a whole much
more easier to reason about.

### Extensible

Last but not least of the defining features of the kubernetes API is its ease of
extensibility.

## Further Reading

* Declarative vs imperative linkys
* Distributed systems declarative etc.

## Exercise

There are no exercises for this part of the workshop, just be sure to have read
and digested the information provided.
