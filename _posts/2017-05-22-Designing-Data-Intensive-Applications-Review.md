---
layout: post
title: Designing Data Intensive Applications Review
category: blog
tags: review
published: true
summary: book review Designing Data Intensive Applications
---
[Safari Books Online](https://www.safaribooksonline.com/library/view/designing-data-intensive-applications/9781491903063/)

![ddia](/public/ddia.jpg)

This is a reference to the first printed edition from March 2017.

Presented at over 500 pages, in three parts, this book is about the building blocks of data systems and the engineering it requires to provide the three pillars of *Reliability*, *Scalability*, and *Maintainability*.

The **big ideas** here are taken from the last 30 years consolidated in Document based, Graph, Relational and Key Value storage systems.

We can expect hybrid solutions that take on the characteristics of more than one model.

**The recurring idea** is that for any given problem there are several solutions, for example, in memory or disk based storage.

The data access patterns presented are relevant for readers who are front-end developers streaming data into the UI and may have already have encountered uni-directional data-flow models like ReactJS.

Distributed computing is most successful where failure is modelled as a first class concept for reliability. Just because traditional database systems use transactions it does not mean that an application is free from end to end data-loss and corruption - there needs to be in place additional countermeasures.

Reading the book is a **journey through** a sometimes pessimistic geography presented as illustrations in the chapters :-

Ocean of Distributed data

Sea of Derived Data

Gulf of Binary Encodings

Bay of Causality

Partitioning Atoll

Wrecks of Homegrown consensus Alogorithms

Harsh Winds of Reality

---

Finally, the book touches on the responsibilty of what we do with the data being collected, since we have access to almost unlimited storage sizes and duration of the analytics across the entire life span of individuals.  
