# Discoverability Ports

## Post

🔎 Discoverability ports are the access point to the data product.

👉 A unique URI must identify each instance of a data product. From this URI it should be possible to automatically trace back to the base URL used by the data product to expose its discoverability ports.

🤓 A potential consumer can read the data product's descriptor document or a specific part of it through the discoverability ports. This way, for example, consumers can discover the data product's other exposed ports (endpoints and APIs).

👇 Similar to observability and control ports, implementing discoverability ports involves a collaborative effort:

👨‍⚖️ 👩‍⚖️ The governance team defines the descriptor structure and the standard APIs of the discoverability ports

👷‍♂️ 👷‍♀️The platform team implements the discoverability sidecar that exposes the descriptor to consumers through standard APIs

👨‍🔧 👩‍🔧 The data product team creates the descriptor and populates it with the required metadata

🤓🔎 Knowing the URI of a data product instance, consumers can directly access its discoverability ports to read specific information about the data product. Alternatively, the platform team can create a catalog by indexing information from discoverability ports, enabling cross-product searches within the product portfolio.

[#TheDataJoy](https://www.linkedin.com/feed/hashtag/?keywords=thedatajoy) **#dataProducts #dataCatalog**

## Image

![2024-P019-composability.png](/images/2024/2024-P038-discoverability-ports.png)

[draw.io](https://app.diagrams.net/) source of the image is available [here](/images/2024/2024.drawio) 

## Follow the conversation

🔵 [Linkedin post](https://www.linkedin.com/posts/andreagioia_thedatajoy-dataproducts-datacatalog-activity-7220079270511947776-4ukz)
