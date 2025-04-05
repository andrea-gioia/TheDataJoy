# Data Product Ports

## Post

Output ports are necessary but not sufficient...

👉 A data product is a software application that exposes one or more relevant data assets, ensuring their accuracy, reusability, and composability. In this sense, the services that expose data, generally called output ports, are certainly the most important. 

✋ However, to fulfill its objectives and be managed in a runtime environment, a data product must also expose the following services or ports:

1️⃣ Input ports: Allow input data to be acquired from upstream sources

2️⃣ Discoverability ports: Expose metadata that statically describes the data product

3️⃣ Observability ports: Expose telemetry data on the operation of the data product

4️⃣ Control port: Allows administrative actions to be performed on the data product, such as granting access permissions or setting configurations

✍ All of these services must be formally described in a descriptor document. Each port, regardless of type, can be described using an API and a set of service agreements of various types (promises, expectations, and obligations).

🤓 The presence of multiple ports beyond output ports and the need to express different types of agreements on these ports are two examples of the reasons why the concept of a data contract must be extended to fully describe a data product. In short, a data product descriptor document should be more than just the set of data contracts that describe its output ports.


[#TheDataJoy](https://www.linkedin.com/feed/hashtag/?keywords=thedatajoy) **#datacontracts #dataproducts**

## Image

![2024-P019-composability.png](/images/2024/2024-P035-Data-product-ports.png)

[draw.io](https://app.diagrams.net/) source of the image is available [here](/images/2024/2024.drawio) 

## Follow the conversation

🔵 [Linkedin post](https://www.linkedin.com/posts/andreagioia_thedatajoy-datacontracts-dataproducts-activity-7212447194728042496-6lOX)
