# A.34.IR46.style.node

**Purpose**: Style shall be mapped to the wms:Style element. The humanreadable name shall be mapped to the wms:Title element and the Unique Identifier shall be mapped to the wms:Name element.

**Prerequisites**

* Test for the existence of default element namespace.

**Test method**

* Check if there is a Title node and a Name node with a Unique Identifier in each Style section.


**Reference(s)**:
* [TG VS](README.md#ref_TG_VS), Chapter 4.2.3.3.4.8
* IR Annex III, Part A, Chapter 2.2.4

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
Title <a name="Title"></a> | /WMS_Capabilities/Capability/Layer/Style/Title
Name <a name="Name"></a> | /WMS_Capabilities/Capability/Layer/Style/Name
Style <a name="Style"></a> | /WMS_Capabilities/Capability/Layer/Style
