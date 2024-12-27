# Hexagonal Architecture

## Post

🤔 Hexagons everywhere, but why?

🤓 In architectural diagrams, data products are typically represented using hexagons. The choice of this shape is not random but stems from the architectural pattern introduced by Alistair Cockburn, known as Hexagonal Architecture.

📕 The Hexagonal Architecture aims to create loosely coupled application components that can be easily connected to their environment by means of ports and adapters.

🎯 By definition, data products are autonomous entities that are as decoupled as possible from their external environment. Just like microservices, they perfectly align with this architectural pattern.

🏹 Specifically, to reduce the cognitive load on the data product teams, it is crucial to isolate them as much as possible from the technological complexities related to interaction with the external environment, allowing them to focus primarily on the development of enrichment and modeling logic for the managed data assets.

👇 To achieve this...

1️⃣ 👨‍⚖️👩‍⚖️ The governance team defines the interfaces and protocols for the ports that handle all interactions between data products and the external environment. 

2️⃣ 👷‍♂️👷‍♀️ The platform team develops the services that implement these ports using appropriate sidecars. 

3️⃣ 👨‍🔧 👩‍🔧The product teams interact only with the sidecars, generally through declarative and technology-agnostic interfaces. Sidecars isolate the business logic from the surrounding environment and mask its complexity.

📌 In previous posts, I’ve described the main types of ports a data product needs, their functions, and how to implement them using sidecars. You can find the links in the comments. 

🔻 If you’ve already developed data product sidecars or have links to useful resources, share them in the comments!

[#TheDataJoy](https://www.linkedin.com/feed/hashtag/?keywords=thedatajoy) **#dataProducts enterpriseArchitecture**

![2024-P019-composability.png](/images/2024/2024-P040-hexagonal-architecture.png)

[draw.io](https://app.diagrams.net/) source of the image is available [here](/images/2024/2024.drawio) 

## Follow the conversation

🔵 [Linkedin post](https://www.linkedin.com/posts/andreagioia_thedatajoy-dataproducts-enterprisearchitecture-activity-7225084293633437696-y1O_)
