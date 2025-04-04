# Data Contract vs. Data Product Specifications
## - Friends, Enemies, or Frenemies?

With the rise of **data mesh**, managing **data as a product** has become a hot topic within the data community. This shift has sparked numerous initiatives to define a common specification for formally describing data assets managed as products.

However, not all specifications approach this in the same way. Some focus primarily on the **data asset itself**, detailing its structure and metadata. Others take a broader perspective, describing the **data product as a whole**, including its exposed services (i.e. **ports**) and internal components.

These two approaches have led to two distinct types of specifications:

- **[Data Contract Specifications]**, which focus on defining the structure of a data asset and all associated metadata.
- **[Data Product Specifications]**, which focus on defining how a data product manages, exposes, and serves its data assets.

In this blog post, I will explore both perspectives using two key examples:

- **The Open Data Contract Standard (ODCS)(https://bitol-io.github.io/open-data-contract-standard/latest/)** from the [Bitol Project](https://bitol.io/) as an example of a data contract specification.
- **[The Data Product Descriptor Specification (DPDS)]((https://dpds.opendatamesh.org/specifications/dpds/1.0.0/)** from the [Open Data Mesh Initiative](https://initiative.opendatamesh.org/) as an example of a data product specification.

By comparing these two approaches, I’ll show why they are not mutually exclusive but can work best when used together.

---
## What makes them different

A pure data product is a software application that focuses on exposing data assets to potential consumers in a way that ensures their relevance, accuracy, usability, and composability over time. In summary, pure data products aim to increase the potential value of managed data assets by making them available for the implementation of multiple use cases over time.

IMAGE

A pure data product manages and makes one or more data assets available for use. Data Contract Specifications (DCS) focus on defining how to describe the data assets being shared, while Data Product Specifications (DPS) focus on how to describe the data products that handle and expose those assets.

IMAGE

A DCS can be used to describe a data asset from multiple perspectives, including:

- The data model
- Constraints applied to different elements of the model
- Quality metrics and corresponding tests
- Quality indicators with associated SLOs/SALs
- Data provenance and static lineage tracking
- Links to other data assets (syntactic links)
- Connections to business terms or concepts (semantic links)

  A DPS, on the other hand, can be used to describe a pure data product from multiple perspectives, including:

- Types of exposed services (ports)
- APIs of the exposed services
- Applicable SLOs/SLAs for the services
- Terms of use
- Billing policies for service usage
- Internal application components
- Internal infrastructure components
- Lifecycle management
- Dependencies between products

To better understand the structure and practical applications of DPS e DCS, let’s explore two concrete examples, analyzing them separately before examining their overlaps and potential integrations.

  



