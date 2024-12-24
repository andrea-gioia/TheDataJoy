# Semantyc Layer

## Post

How much **#semantics** your **#semanticlayer** can handle?

🔴 Most of the semantic layers I've come across in my professional experience act more like a syntactic layer than a semantic one. They introduce very little semantics. They simply federate data sources by creating a unified model that translates the different physical models using terminology that is more understandable to the business. The semantics remain partly in the developers' heads and partly in the code they write to translate the physical models into the business-friendly model exposed to consumers.

⭕ Some modern semantic layers allow defining the model exposed to consumers declaratively, relying on predefined models generally based on variants of the dimensional model. In this case, the semantic contained in the translation logic is somewhat easier to understand. However, such semantics are primarily for documentation purposes. Consumers do not effectively use it. Thus, the semantic layer remains also in this case little more than a data virtualization tool.

❤️ A true semantic layer should allow the defining of a semantic model (TBox) consisting of conceptually rich concepts and relationships between concepts (not just generic FK relationships) that are easily extensible. This model should then be linked to physical data through semantic linking (ABox), forming a hashtag#knowledgegraph. The query engine should use the knowledge graph to translate queries made at the conceptual model level into federated queries on the physical data present in the source systems.

🤓 Building a true semantic layer today requires the integration of hashtag#dataCatalog, hashtag#graphDatabase, and hashtag#dataVirtualization tools. Graph databases and their extensions for managing knowledge graphs among the three families of products seem to be the most advanced and well-positioned to provide an integrated semantic layer in a single solution. However, they are also the least common class of used products in my experience. Is it just a matter of time, or do you think there are other reasons? 🤷‍♂️


[#TheDataJoy](https://www.linkedin.com/feed/hashtag/?keywords=thedatajoy) 

## Image

![2024-P018-semantic-layer.png](/images/2024/2024-P018-semantic-layer.png)

[draw.io](https://app.diagrams.net/) source of the image is available [here](/images/2024/2024.drawio) 

## Follow the conversation

🔵 [Linkedin post](https://www.linkedin.com/posts/andreagioia_semantics-semanticlayer-knowledgegraph-activity-7161759271976747008-CtQw?utm_source=share&utm_medium=member_desktop)



