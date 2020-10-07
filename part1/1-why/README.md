# Part 1.1: An Understanding of Why the Kubernetes API Is So Good

## About

There are a number of qualities that make the kubernetes API so attractive.

### Declarative

The first is that it is a declarative API; when interacting with the API you
tell it _what_ you want, not _how_ to do what you want. One great advantage to
declarative APIs is that they allow you to store your declarations in version
control systems, such as Git, thereby bringing all the benefits of version
control (record of changes, rollback, code history, etc.) to the table. This
pattern is sometimes referred to as GitOps.

### Level-based

The second great quality of the API is that it is "level-based", as opposed to
"edge-based". In level-based systems, components react to the current observed
state of the world, and as such, do not need to rely on previously-observed
states in order to make decisions. In short the benefit of this is that
level-based systems are much more resilient in the face of disruption. This is
not typically true of edge-based systems. The article, "[Level Triggering and
Reconciliation in
Kubernetes](https://hackernoon.com/level-triggering-and-reconciliation-in-kubernetes-1f17fe30333d)"
provides a really great overview of level-based vs edge-based systems and is
great reading on the subject.

### Separation of state

The kubernetes API separates its state into two - desired state and observed
state. Users of the API (human or machine) express a desired state and the
system continually works to make it so. As the system works it reports the
current observed state. This clear separation and simple state model makes the
system easier to reason about.

### Extensible

Last but not least of the defining features of the kubernetes API is its ease of
extensibility, primarily (although not exclusively) through CRDs and custom
controllers. This ease of extensibility is the driving force behind the
"kubernetes-native" style of programming and system design that we are seeing
evolve, and that we will be exploring throughout the remainder of this workshop.

## Further Reading

* Declarative vs imperative linkys
* Distributed systems declarative etc.
* https://medium.com/@graemecolman/the-new-kubernetes-native-d19dd4ae75a0
* https://developers.redhat.com/blog/2020/04/08/why-kubernetes-native-instead-of-cloud-native/

## Exercises

There are no exercises for this part of the workshop, just be sure to have read
and digested the information provided.
