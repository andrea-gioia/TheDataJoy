# Input and Output Ports

## Post

💫 It is between the input and output ports that the magic of data products happens.

🔀 Input ports are responsible for reading data from upstream source systems, while output ports expose the produced data to downstream consumers.

✋ Generally, the product team implements pipelines that source data, transform it, and then serve it to consumers. However, to reduce the cognitive load on product teams and make development faster, it is better to manage input and output ports in the following way...

1️⃣ 
👨‍⚖️ The governance team defines how to specify declaratively in the descriptor document which sources to use, what data to acquire, when to acquire it, and in which internal storage (landing data stores) it should be deposited once read.
👩‍⚖️ The governance team also defines how to specify declaratively in the descriptor document where the produced data is stored (serving data stores) and through which APIs it should be exposed for consumption.

2️⃣ 
👷‍♂️ The platform team implements a sourcing sidecar capable of interpreting the specifications for the input ports in the descriptor document and acquiring the data accordingly.
👷‍♀️ The platform team also implements a serving sidecar capable of interpreting the specifications for the output ports in the descriptor document and implementing services that expose the produced data accordingly.

3️⃣ 
👨‍🔧 👩‍🔧 At this point, the data product team only needs to specify their requirements in the descriptor for sourcing and serving. They then implement pipelines that read from the sourcing data stores when triggered by the sourcing sidecar and activate the serving sidecar once they have finished writing the produced data to the consumption data stores.

🎁 BONUS: Sourcing and serving sidecars, in addition to helping data product teams, can contain many extra features that are useful to the platform team for monitoring and controlling data traffic between products, similar to what is done by the proxy in a Service Mesh architecture (e.g., Dynamic DP discovery, TLS termination, Circuit breakers, Health checks, Fault injection, Rich metrics, etc..).

[#TheDataJoy](https://www.linkedin.com/feed/hashtag/?keywords=thedatajoy) **#dataProducts##

![2024-P019-composability.png](/images/2024/2024-P039-in-and-output-ports.png)

[draw.io](https://app.diagrams.net/) source of the image is available [here](/images/2024/2024.drawio) 

## Follow the conversation

🔵 [Linkedin post](https://www.linkedin.com/posts/andreagioia_thedatajoy-dataproducts-activity-7222601575033167872-YRfK)
