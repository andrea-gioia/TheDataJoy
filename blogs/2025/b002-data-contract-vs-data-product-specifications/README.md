# Data Contract vs. Data Product Specifications: Friends, Enemies, or Frenemies?

With the rise of **data mesh**, managing **data as a product** has become a hot topic within the data community. This shift has sparked numerous initiatives to define a common specification for formally describing data assets managed as products.

However, not all specifications approach this in the same way. Some focus primarily on the **data asset itself**, detailing its structure and metadata. Others take a broader perspective, describing the **data product as a whole**, including its exposed services (i.e. **ports**) and internal components.

These two approaches have led to two distinct types of specifications:

- **Data Contract Specifications**, which focus on defining the structure of a data asset and all associated metadata.
- **Data Product Specifications**, which focus on defining how a data product manages, exposes, and serves its data assets.

In this blog post, I will explore both perspectives using two key examples:

- **[The Open Data Contract Standard (ODCS)](https://bitol-io.github.io/open-data-contract-standard/latest/)** from the [Bitol Project](https://bitol.io/) as an example of a data contract specification.
- **[The Data Product Descriptor Specification (DPDS)](https://dpds.opendatamesh.org/specifications/dpds/1.0.0/)** from the [Open Data Mesh Initiative](https://initiative.opendatamesh.org/) as an example of a data product specification.

By comparing these two approaches, I’ll show why they are **not mutually** exclusive but can work **best when used together**.

---
## What makes them different

A **pure data product** is a software application that focuses on exposing data assets to potential consumers in a way that ensures their **relevance**, **accuracy**, **usability**, and **composability** over time. In summary, pure data products aim to increase the potential value of managed data assets by making them available for the implementation of multiple use cases over time.

![Pure Data Products](./images/2025-B002-01-pure-data-product.png)

A pure data product manages and makes one or more data assets available for use. **Data Contract Specifications (DCS)** focus on defining how to describe the data assets being shared, while **Data Product Specifications (DPS)** focus on how to describe the data products that handle and expose those assets.

![DPS vs DCS](./images/2025-B002-02-dps-vs-dcs.png)

A DCS can be used to describe a **data asset** from multiple perspectives, including:

- The data model
- Constraints applied to different elements of the model
- Quality metrics and corresponding tests
- Quality indicators with associated SLOs/SALs
- Data provenance and static lineage tracking
- Links to other data assets (syntactic links)
- Connections to business terms or concepts (semantic links)

  A DPS, on the other hand, can be used to describe a **pure data product** from multiple perspectives, including:

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

## Open Data Contract Standard

**Open Data Contract Standard (ODCS)** is a well-known example of a Data Contract Standard (DCS) developed by the [Bitol Project](https://bitol.io/).

![Open Data Contract Standard (ODCS)](./images/2025-B002-03-odcs.png)

In ODCS’s [metamodel], a data asset is represented as an **object** with various **properties**. Each property has a **unique name** within its object and a defined **data type**. The type can be either primitive (e.g., `int`, `string`, `boolean`) or composite (e.g., `object` or `array`).

Thanks to this flexible structure, ODCS can describe both **tabular data assets** — where entries consist solely of primitive types — and **document-based data assets**, where entries can include composite types, creating a nested structure instead of a simple flat one.

To define the structure of a specific data asset, ODCS uses [JSON Schema](https://github.com/bitol-io/open-data-contract-standard/blob/main/schema/odcs-json-schema-latest.json) as its schema definition language (SCD) preferring YAML over JSON as the encoding format.

```yaml
version: 1.0.0

schema:
  - name: tbl
    logicalType: object
    properties:
      - name: txn_ref_dt
        logicalType: date
      - name: rcvr_id
        logicalType: string
      - name: rcvr_cntry_code
        logicalType: string
```

Structural elements of the model can be enriched with various descriptive metadata, grouped into the following ten main schema annotation vocabularies:

- **Fundamentals** (e.g., name, version, descriptions…)
- **Schema** (logical and physical metadata)
- **Data Quality** (data quality rules and data governance policies)
- **Pricing** (internal or external costs associated with usage)
- **Team** (history of team members)
- **Security** (roles)
- **SLA** (latency, retention, frequency…)
- **Infrastructure** (servers, environment, and storage)
- **Business Rules** (data QoS applied to specific business needs)
- **Custom** (space for custom needs)

A data contract instance in ODCS is therefore the combination of the structural description of the data asset along with all the relevant metadata needed for its management and usage.

![Elements of an ODCS v3 valid instance](./images/2025-B002-04-odcs-metamodel.png)

Here you can find a [complete example of a data contract instance](https://bitol-io.github.io/open-data-contract-standard/latest/examples/all/full-example.odcs.yaml) compliant with the ODCS.

## Data Product Descriptor Specification

**Data Product Descriptor Specification (DPDS)** is a well-known example of a Data Product Specification (DPS) developed by the [Open Data Mesh Initiative](https://initiative.opendatamesh.org/).

![Data Product Descriptor Specification (DPDS)](./images/2025-B002-05-dpds.png)

Since there is no single, universally accepted definition of a data product, all existing DPSs take an opinionated approach to how a data product should be structured and what its key components are. That said, the main DPSs currently available largely align with the concept of pure data products, where each product is made up of interfaces, often grouped into ports, and internal components, typically divided into application and infrastructural components.

![Pure Data Product Structure](./images/2025-B002-06-pure-data-product-anatomy.png)

DPDS follows this vision of data product structure in defining its metamodel, which is illustrated at a high level in the following image.

![DPDS Metamodel](./images/2025-B002-07-dpds-meta-model.png)

Specifically, the DPDS metamodel describes a data product through a descriptor object that is composed of

1. one object that contains all general information about the data product (**Info Object**),
1. six types of ports (**Input, Output, Discoverability, Observability, and Control Ports**),
1. three types of internal components (**Lifecycle Info, Application Components, and Infrastructural Components**).

To define the structure of a specific data product, DPDS uses [JSON Schema](https://dpds.opendatamesh.org/specifications/dpds/1.0.0/schema/) as its schema definition language (SCD) accepting both YAML and JSON as encoding formats. 

```json
{
    "dataProductDescriptor": "1.0.0",

    "info": {
        "name": "tripExecution",
        "fqn": "urn:dpds:com.company-xyz:dataproducts:tripExecution:1"
    },

    "interfaceComponents": {
      "inputPorts": [{
        "name": "transportManagementSystem"
        "fqn": "urn:dpds:com.company-xyz:dataproducts:tripExecution:1:outputports:transportManagementSystem",
      }]
      "outputPorts": [{
        "name": "tripStatus",
        "fqn": "urn:dpds:com.company-xyz:dataproducts:tripExecution:1:outputports:tripStatus",
      }]
   },

   "internalComponents": {
     "applicationComponents": [{
       "name": "cdcIngestionApp",
       "fqn": "urn:dpds:com.company-xyz:dataproducts:tripExecution:1:applications:cdcIngestionApp",
     },{
       "name": "eventProcessorApp",
       "fqn": "urn:dpds:com.company-xyz:dataproducts:tripExecution:1:applications:eventProcessorApp",
     }{
       "name": "dbSinkConnectorApp",
       "fqn": "urn:dpds:com.company-xyz:dataproducts:tripExecution:1:applications:dbSinkConnectorApp",
     }],
     "infrastructuralComponents": [{
       "name": "eventStore",
       "fqn": "urn:dpds:com.company-xyz:dataproducts:tripExecution:1:infrastructure:eventStore",
     },{
       "name": "stateStore",
       "fqn": "urn:dpds:com.company-xyz:dataproducts:tripExecution:1:infrastructure:stateStore",
     }]
  }
}
```

Like ODCS, DPDS not only defines the structure of the object of interest — in this case, a data product — but also allows for enriching it with additional metadata. To achieve this, keywords used for annotation are organized into vocabularies, grouping them based on function or the element they describe (e.g., API, SLO, usage, contact points, etc.).

In DPDS, each component of a data product has its dedicated vocabulary or set of associated vocabularies. For instance, every port, regardless of its specific type, can be annotated using keywords defined in one of the following three vocabularies:

1. **Promises:** Contains all the keywords useful for specifying the intent of the port. Promises are not a guarantee of the outcome but the data product will behave accordingly to them to realize its intent. Examples of annotations defined in promises vocabulary are API, SLO, deprecation policy, etc.
    
1. **Expectations:** Contains all the keywords useful to specify how the port should be used by consumers. They are a way to explicitly state what promises the data product would like consumers to make regarding how they will use the port. Examples of annotations defined in expectations vocabulary are intended usage, intended audience, etc.

1. **Obligations:** Contains all the keywords useful to specify promises and expectations that must be respected both by the data product and its consumers respectively. An obligation is an explicit agreement between the data product and its consumers. It is used to group all the promises and expectations that if not respected can generate penalties like monetary sanctions or interruption of service. Examples of annotations defined in obligations vacabulary are terms of conditions, SLA, billing policy, etc.
Here you can find a complete example of a data product described using DPDS.

## Common overlaps
Since, in managing the data-as-a-product paradigm, data assets and data products are closely related, it is natural for the two types of specifications to have some overlaps, even though their primary focus is on describing different objects.



