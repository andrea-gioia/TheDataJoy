# How to Define Internal Data Specifications to Govern Your Data Ecosystem: Hands-on Guide

In the world of data, we have plenty of specifications — but surprisingly few standards. SQL is one of the rare success stories, a standard that has saved countless resources over the years thanks to its interoperability. But beyond SQL, widely adopted standards are scarce, and this gap poses a major challenge for the entire ecosystem.

Why is this happening? And what can we do to change it? In my next post, I’ll explore ways to foster new standards in the data space. But first, let’s take a step back. What makes a good data specification? And how can you build one from scratch within your organization? In this post, I’ll break down the key elements of an effective specification and share practical steps to create one.

---

## What Is a Specification Anyway?

A specification is a formal and unambiguous description of an entity of interest, either an object or a process, that provides all and only the necessary information for its design, development, and/or operational use.

A **specification** can be either public or private. A **public specification** is considered **open** when its evolution isn’t controlled by a single organization but is shaped by multiple organizations through clear and inclusive governance rules.

A **standard** is an open specification that multiple organizations within a shared ecosystem widely adopt. It is typically recognized by a standardization body that oversees its evolution through a collaborative and transparent process.


## Why Internal Data Specifications Matter

Data specifications are fundamental to ensuring that a data solution or data product is built correctly, meets expectations, and remains easy to use and maintain over time. In many ways, they represent the highest form of **global governance policies**.

Their importance grows in complex data ecosystems where multiple independent entities operate in a distributed manner, often with different — or even conflicting — goals. In these environments, shared specifications serve as the **rules of the game**, imposing certain constraints on individual actors in exchange for smoother collaboration and a more sustainable evolution of the entire data ecosystem.

Even without widely accepted **data standards**, defining **internal data specifications** can be highly valuable for an organization looking to govern its **data ecosystem** — especially when adopting a **data-as-a-product** paradigm or embracing **data mesh** principles.


## How to Get Started

When defining an internal specification, the first step is to clearly understand what you are describing and why it needs to be defined. Once that’s established, the next step is determining who should be involved in the process.

Internal specifications are best developed in a **collaborative**, **federated approach**, actively involving representatives from all impacted groups rather than imposing them from the top down. Even within an organization, a specification only makes sense if it is actually used — and the best way to ensure adoption is to engage stakeholders in its creation.

Defining an internal specification doesn’t always mean starting from scratch — in fact, quite the opposite. Once the **what** and **why** are clear, it’s crucial to carefully consider the **how**. This involves assessing whether existing external specifications already meet the identified requirements. While no external specification will perfectly fit every organization’s needs, it’s important to weigh the **trade-offs** between adapting an existing one and building a new specification from the ground up.

Once a shared decision is reached, it should be documented for future reference through a **governance decision record**.

If there are strong reasons not to reuse an existing specification, it’s time to move forward with designing an internal **custom specification**. Let’s explore how.

## Designing Your Own Data Specification
Specifications can be broadly categorized into two types, depending on the entity being described: **object specifications** and **protocol specifications**.

An **object specification** outlines the attributes, properties, behaviors, and constraints of an object (ex. [Data Product Descriptor Specification](https://dpds.opendatamesh.org/)). A **protocol specification**, on the other hand, defines the rules and formats that different actors must follow to communicate with one another (ex. [Open Telemetry Protocol](https://opentelemetry.io/docs/specs/otel/protocol/)).

In short, **object specifications** describe the components of a system, while **protocol specifications** explain how these components interact.

In this blog post, we’ll focus on defining an **object specification** in the data context. Object specifications are simpler, something I’m quite familiar with from writing several of them, and they often serve as the foundation for more complex **protocol specifications**.

An object specification should clearly and unambiguously define how to describe the object of interest. In my experience, this can be achieved by defining the following three key elements in the specification:

🗺️ A Metamodel

📜 A Schema Definition Language (SDL)

📚 Schema Annotation Vocabularies

Let’s take a closer look at each of these.
