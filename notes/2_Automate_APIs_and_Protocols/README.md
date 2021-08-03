# 2.0 Automate APIs and Protocols

[Identify the JSON instance based on YANG model](01_Identify_the_JSON_Instance_Based_on_YANG_Model.md)
[Identify the XML instance based on YANG model](02_Identify_the_XML_Instance_Based_on_YANG_model.md)
[Interpret a YANG module tree generated per RFC8340](03_Interpret_a_YANG_Module_Tree_Generated_Per_RFC8340.md)
[Compare functionality benefits of OpenConfig, IETF, and native YANG models](04_Compare_Functionality_Benefits_of_Open_and_Native_YANG_models.md)
[Compare functionality benefits and uses of NETCONF and RESTCONF](05_Compare_Functionality_Benefits_and_Uses_of_NETCONF_and_RESTCONF.md)





## Why data models?

- Cli commands return data in human-readable format, but output varies depending on vendor, model, OS, etc
- To automate/program the network, the endpoints (e.g. switches and the automation server) need to agree on:
  - protocol: NETCONF, RESTCONF, RESTAPI, SOAP
  - Data format: XML, JSON, etc
  - Data model: Aggreed-upon structure of the data so that both endpoints understand each other
