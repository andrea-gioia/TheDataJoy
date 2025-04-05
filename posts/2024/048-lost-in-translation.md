# Lost in translation

## Post

😫 Don't get lost in translation...

✍ Each business subdomain should define a conceptual model (👉 subdomain ontology) to describe the data exposed by its data products explicitly. This allows external consumers to understand the meaning of the data and use it independently, without needing to ask for clarification from the developers who created the data product.

✋ However, each domain has its own language (👉 ubiquitous language) and perspective on the concepts it represents, influenced by its specific context. Even when different domains represent the same concepts, they often do so in different ways.

😵 As a result, a consumer who wants to combine data from two different subdomains must first translate the concepts from one subdomain into the other or, more commonly, translate the concepts from both source subdomains into those of their own subdomain (👉 ontology mapping). This translation process is time-consuming and prone to errors.

✌ It is generally more effective to centralize this translation task by defining a shared domain ontology to enhance semantic interoperability between the data exposed by different domains. This ontology would contain the key business concepts defined at a general level, which subdomains can then use as a foundation for creating their more specific concepts. Doing so facilitates the interoperability of subdomain ontologies and, consequently, the composability of data products.

💫 The concepts within the domain ontology can be organized by knowledge domains. For each knowledge domain, it's advisable to establish a federated modeling team, consisting of at least one representative from each domain for which the concepts in that knowledge domain are relevant. While product teams are stream-aligned, federated modeling teams, like federated governance teams in data mesh-oriented approaches, are enabling teams.

[#TheDataJoy](https://www.linkedin.com/feed/hashtag/?keywords=thedatajoy) **#dataProducts #knowledgeEngineering #ontology #teamTopologies**

## Image

![2024-P019-composability.png](/images/2024/2024-P048-lost-in-translation.png)

[draw.io](https://app.diagrams.net/) source of the image is available [here](/images/2024/2024.drawio) 

## Follow the conversation

🔵 [Linkedin post](https://www.linkedin.com/posts/andreagioia_thedatajoy-dataproducts-knowledgeengineering-activity-7236727242582577152-Sytl)
