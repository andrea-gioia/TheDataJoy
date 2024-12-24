# Semantic linking: by copy or by reference?

## Post
🤔 Should factual data be added to a knowledge graph by copy or by reference?

🤓 A knowledge graph (KG) encapsulates both abstract concepts coming from ontology and factual data stored in corporate systems.

1️⃣ In a federated modeling model, the responsibility of defining the ontology is owned by a central team, while the responsibility of defining the links between factual data and ontology concepts is distributed among individual data product teams.

2️⃣ The self-serve data-ops platform, every time a new data product is published, uses semantic links defined in the data product's contract to extend the KG. This operation can be done in two ways...

🔴 By copy
For each row in the dataset exposed by the data product, a new instance is created within the KG. The data from the company's systems is essentially copied into the KG.

🔵 By reference
Within the KG, an instance of a concept representing a dataset and possibly the data service exposing it in the model is added, for example using DCAT vocabulary. The data is not copied into the KG, but the source where it exists at the physical level is simply referenced.

Which approach do you prefer and why? What are the advantages and disadvantages of one approach over the other? 🔴🔵


[#TheDataJoy](https://www.linkedin.com/feed/hashtag/?keywords=thedatajoy) **#knowledgegraphs #datacontracts #dataproducts #datamodelling**

## Image

![2024-P011-01-LinkingByCopy.png](/images/2024/2024-P011-01-LinkingByCopy.png "ByCopy")

[draw.io](https://app.diagrams.net/) source of the image is available [here](/images/2024/2024.drawio) 


![2024-P011-02-LinkingByReference.png](/images/2024/2024-P011-02-LinkingByReference.png "ByReference")

[draw.io](https://app.diagrams.net/) source of the image is available [here](../images/013-LinkingByReference.drawio) 

## Follow the conversation

🔵 [Linkedin post](https://www.linkedin.com/feed/update/urn:li:activity:7133825401864265728/)
