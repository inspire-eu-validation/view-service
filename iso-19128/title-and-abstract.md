# Title and Abstract

**Purpose**: A View Service must contain a non-empty Title and Abstract to fulfill the INSPIRE Metadata requirements for Resource Title, Resource Abstract and Spatial Resolution.

**Prerequisites**

* [Schema validation](./schema-validation.md)

**Test method**
* Check that both [Title](#title) and [Abstract](#abstract) exist and are non-empty.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.1, Requirement 10

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Title <a name="title"></a> | ./wms:Service/wms:Title
Abstract <a name="abstract"></a> | ./wms:Service/wms:Abstract
