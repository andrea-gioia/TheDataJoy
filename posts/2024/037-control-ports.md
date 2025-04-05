# Control Ports

## Post

🎮 Control port: when just observing data products is not enough

👉  Data products leverage control ports for dynamic management at runtime. These ports grant access permissions to output ports, enable administrative actions (e.g., adding local policies, deleting data), and configure internal components (e.g., quality checks execution frequency).

🤚 Control ports empower administrators to adapt a data 
product's behavior after deployment, but within the boundaries defined in the released descriptor document. Any significant deviations require modifying the descriptor document and releasing a new data product version.

👇 Similar to observability ports, control ports involve a collaborative effort:

👨‍⚖️ 👩‍⚖️ Governance Team: Defines control port APIs and standardizes actions/configurations each data product must handle.

👷‍♂️ 👷‍♀️ Platform Team: Develops a control sidecar implementing governance APIs. This sidecar translates requests into actions or configuration changes through a mediator.

👨‍🔧 👩‍🔧 Product Team: Implements internal components that utilize configurations exposed by the sidecar and expands it with actuators. These actuators translate external requests into actions on internal components.

📌 In essence, control ports provide a flexible yet controlled approach to managing data products at runtime.

[#TheDataJoy](https://www.linkedin.com/feed/hashtag/?keywords=thedatajoy) **#dataProducts**

## Image

![2024-P019-composability.png](/images/2024/2024-P037-control-ports.png)

[draw.io](https://app.diagrams.net/) source of the image is available [here](/images/2024/2024.drawio) 

## Follow the conversation

🔵 [Linkedin post](https://www.linkedin.com/posts/andreagioia_thedatajoy-dataproducts-activity-7217547690694316033-LUmB)
