---
layout: post
title: Clojure Applied Review
category: review
tags: clojure review
published: true
summary: Clojure Applied Review - From Practice to Practitioner
---

![Clojure Applied Book](https://raw.githubusercontent.com/griffio/griffio.github.io/master/public/clojure_applied.jpg)

### [Clojure Applied](https://pragprog.com/book/vmclojeco/clojure-applied)

Authors [Ben Vandgrift](https://twitter.com/bvandgrift) & [Alex Miller](https://twitter.com/puredanger).

#### This is an overview of the first printed book available (Sept 2015) containing 211 pages

* Foundations
* Applications
* Practices
* Appendices

Since I am moving on from [Living Clojure](https://griffio.github.io/review/2015/05/02/Living-Clojure-Review/); How is “Clojure Applied” different to the [dozen or so Clojure books](http://clojure-doc.org/articles/ecosystem/books.html) released so far?

**It does not follow any ‘Cookbook’ style**; instead the "Foundations" and "Applications" parts are sequential in approach. The Third part titled “Practices” describes reference material for production use. Finally, the Appendices contain the philosophy behind Clojure and the precise nature of its design and vocabulary.

**This is for the intermediate Clojurist**; who is familiar with the syntax - has solved puzzles in the REPL - ready to begin their journey into real development practices.

**From Practice to Practitioner** is the subtitle of "Clojure Applied"; an introduction in this book proposes that the commitment to learning the Clojure way of thinking begins in a longer middle stage of real work. 

**As part of the Pragmatic Bookshelf** series the writing tone in “Clojure Applied” follows the question - What is the problem space this book is trying to solve?

#### First Part: Foundations

The core concepts presented across three chapters begin with modelling domain entities, then, grouping entities with the immutable collection of our choice; finally applying sequential processing with transformational functions. 

**We learn the key abstraction in Clojure is a Sequence.**

For efficiency or performance reasons, some alternative implementations are discussed with additional library support:- clojure.lang.PersistentQueue, [Transients](http://clojure.org/transients), [Medley](https://github.com/weavejester/medley).

This first section doesn’t build up a single application throughout, instead the authors illustrate modelling with some example domains e.g. Money, Customer, Cart, Orders and even trying out Planetary exploration!

Finally, these idioms are illustrated - pulled together - as a "Customer shopping cart" domain example using reducers to produce a final revenue style report.

#### Second Part: Applications

There are four chapters here to answer the question:

**How to build up an application in Clojure**?

The essence of this practice is to model your domain data, transform it with functions, apply structure with namespaces and components to manage state, and encourage use of parallelism across available cores. 

A Clojure application brings together "State and Identity" applied with techniques for managing change in the model data.

Transactional units of work and concurrency combined with parallelism using [reducers](http://clojure.org/reducers) show the advantage of immutable data.

**There are half a dozen diagrams** throughout to illustrate the effect of asynchronous programming models.

Both namespaces and components are structural tools; components are not native to the Clojure language they are containers for state applied in the developers own problem space.

Libraries that are likely to be essential for use in this phase:-

* [StuartSerria/Component](https://github.com/stuartsierra/component) - lifecycle for stateful components.
* [Prismatic/Schema](https://github.com/Prismatic/schema) type metadata validation helps with data conforms to a model.
* [Environ](https://github.com/weavejester/environ) - environment configuration values

#### Third Part: Practices
In three chapters covering testing, data interoperation and deployment.

**Testing** - [clojure.test](https://clojure.github.io/clojure/clojure.test-api.html) with assertions vs expectations, also considers Property based testing with [test.check](https://github.com/clojure/test.check).  

**Formatting Data** - Probably my favourite section, Clojure is special with a first class interop story; Edn, Json and [Transit](https://github.com/cognitect/transit-format) serialisation formats have good coverage here.

**Macros are not covered** in this book as a development practice; one area where the book intentionally doesn’t go.

**Packaging, Publishing and Deployment** coverage is wide ranging from PAAS providers to traditional Application Servers.
One example mentioned is [Immutant.org](http://immutant.org/) from Red Hat Inc. This is close to an integrated stack distribution of Clojure libraries.

#### Appendices 1 & 2
The appendices discuss the roots of Clojure influenced from LISP and the elements that make up the Clojure Language. The process of “Practicing and Thinking” in Clojure is guided by core principles outlined in the second appendix.

**What is a Practitioner**?
A Practitioner will often choose the most direct idiomatic solution rather than the one that involves mastery of the implementation. Although the book only mentions “Practitioner” in the title, completing the book, we can take it to mean a professional developer who specialises in the application of Clojure within their team’s project or open source software.
