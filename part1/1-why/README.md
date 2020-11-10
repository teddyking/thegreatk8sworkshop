# Part 1.1: An Understanding of Why the Kubernetes API Is So Good

## About

There are a number of qualities that make the kubernetes API so attractive.

### Declarative

The first is that it is a declarative API; when interacting with the API you
tell it _what_ you want, not _how_ to do what you want. One great advantage to
declarative APIs is that they allow you to store your declarations in version
control systems, such as Git, thereby bringing all the benefits of version
control (record of changes, rollback, code history, etc.) to the table. This
helps to support [GitOps](https://www.weave.works/technologies/gitops/)
workflows.

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

## Kubernetes-native (TODO: is this its own section?)

The term "kubernetes-native" is a relatively new one, and as such is still open
to interpretation. During this workshop we consider the term through two
different lenses. The first lens considers kubernetes-native software from the
perspective of a single developer or small team - how to write kubernetes-native
software and the pros/cons of doing so. The second lens considers the bigger
picture - the perspective and impact of kubernetes-native software to multiple
teams or groups of people who are all working together. This is really where we
see a lot of the real, true value of "kubernetes-native" software coming to
light.

With that in mind, let's try to define what we mean by kubernetes-native
software. Kubernetes-native software can be thought of as:

> Software that is written specifically to run on, and to take full advantage of
> the kubernetes API

There are lots of benefits to writing software like this. There's also one big
drawback, which we'll touch on in a moment, but let's start by discussing the
good things.

First and foremost is that by choosing to build on top of the kubernetes API,
you can rely on it to provide a number of traditionally complex features for
you, such as:

* Storage of state - the kubernetes API is backed by an etcd datastore
* High Availability - when deployed as part of a cluster of nodes, the
  kubernetes API is highly available
* Extensibility - as discussed above, the kubernetes API is very easy to extend,
  which makes it easy to improve
* Consistent user experience - close integration with the kubernetes tooling
  users already know and love

These are all things that would have historically required a lot of thought and
time to get right. Now, obviously there's no such thing as a free lunch, and
consideration will still need to be given to each of these with regards to
whatever piece of software you're building. However with kubernetes-native
software the bulk of the complexity is baked into the underlying API, leaving
you time and energy to focus on the things you really care about.

This idea is discussed and presented in more detail in, ["To Crd, or Not to Crd,
That is the Question"](https://www.youtube.com/watch?v=xGafiZEX0YA).

One concern often raised when talking about kubernetes-native software is that
it is a large dependency to take on, and that while kubernetes is very much in
vogue right now, we can never be entirely sure of its longevity.

It's a valid concern, one of the first things we learn about writing software is
to try not to couple our code to too tightly to anything else, and yet here's
kubernetes-native software asking us to couple it to an entire IaaS++! (TODO:
better wording).

A counterpoint to this argument is that today, kubernetes is ubiquitously
available. All major infrastructure providers have a kubernetes offering, across
both public and private clouds.

This ubiquitous availability of the kubernetes API feeds nicely into the whole
ethos of kubernetes-native, it's what provides that level of abstraction above
the infrastructure layer, and enables portability of kubernetes-native
applications across clouds.

## Further Reading (TODO)

* Declarative vs imperative linkys
* [GitOps](https://www.weave.works/technologies/gitops/)
* Distributed systems declarative etc.
* https://medium.com/@graemecolman/the-new-kubernetes-native-d19dd4ae75a0
* https://developers.redhat.com/blog/2020/04/08/why-kubernetes-native-instead-of-cloud-native/

## Exercises

There are no exercises for this part of the workshop, just be sure to have read
and digested the information provided.
