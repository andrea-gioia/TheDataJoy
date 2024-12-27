# Enterprise Knowledge Graph Architectures

## Post
✨ Operationalizing the information architecture

👇 There are three main ways to operationalize the information architecture, depending on how the data plane and knowledge plane interact with each other and with external applications:

1️⃣ Data-Centric Solution 👉 data and knowledge are centralized and shared by applications. Data is directly represented within the ontology as instances of the business concepts it defines. Operational and analytical applications access and manipulate the data through the central ontology.

2️⃣ Knowledge Warehouse Solution 👉 operational applications manage their own data independently. Integration processes then extract this data from the applications' data stores and load it into the central ontology as instances of the defined business concepts. Analytical applications can then query the central ontology directly to access the data through a unified model.

3️⃣ Ontology-Based Data Access Solution 👉 data managed by individual operational applications is extracted and made available to potential consumers through hashtag#dataProducts. The data exposed by these products isn’t loaded into the central ontology but is instead linked to the business concepts defined within it. This allows analytical applications to query the ontology, which in turn translates these queries into requests to the external data products, without needing to materialize the data within the ontology itself.

🕸 In all three solutions, the combination of the data plane with the knowledge plane forms a hashtag#knowledgeGraph. In the first two cases, this results in a materialized knowledge graph, where the data is stored within the ontology. In the third case, it forms a virtual knowledge graph, where the data is merely referenced by the ontology and remains within the source systems that manage it.

😉 Which solution is best to operationalize the information architecture depends on the specific context.

[#TheDataJoy](https://www.linkedin.com/feed/hashtag/?keywords=thedatajoy) **#KnowledgeEngineering #DataManagement**

![2024-P019-composability.png](/images/2024/2024-P053-ekg-architectures.png)

[draw.io](https://app.diagrams.net/) source of the image is available [here](/images/2024/2024.drawio) 

## Follow the conversation

🔵 [Linkedin post](https://www.linkedin.com/posts/andreagioia_dataproducts-knowledgegraph-thedatajoy-activity-7240035719644098560-hU-D)
