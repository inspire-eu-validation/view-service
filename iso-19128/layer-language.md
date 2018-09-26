# Layer language

**Purpose**: The layer must be described in a language and terms the users are expected to understand.

**Prerequisites**

* [Schema validation](./schema-validation)

**Test method**

For each Layer element check that the [Abstract element](#Abstract) is a non-empty character string.

**Reference(s)**:

* [TG VS](./README#ref_TG_VS), Chapter 4.2.3.3.4.2, Requirement 34

**Test type**: Automated

**Notes**

This a the description of the layer (a portrayal), not the same thing as the metadata record of the dataset which the layer is visualising.

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Abstract <a name="Abstract"></a> | ./wms:Capability/wms:Layer/wms:Abstract
