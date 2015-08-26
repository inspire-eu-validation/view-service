# A.29.IR34.layer.abstract.node

**Purpose**: Text describing the layer. Subject to multilingualism. It shall be mapped with the wms:Abstract element.

**Prerequisites**

* Test for the existence of default element namespace.

**Test method**

* Check if there is an Abstract node in each Layer section.

**Reference(s)**:
* [TG VS](README.md#ref_TG_VS), Chapter 4.2.3.3.4.2

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
Abstract <a name="Abstract"></a> | /WMS_Capabilities/Capability/Layer/Abstract
Layer <a name="Layer"></a> | /WMS_Capabilities/Capability/Layer
