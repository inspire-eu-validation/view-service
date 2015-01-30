# A.33.IR33.layer.title.node

**Purpose**: Layer title is mapped with wms:Title. The harmonised title of a layer for an INSPIRE spatial data theme is defined by INS DS and shall be subject to multilingualism (translations shall appear in each mono-lingual capabilities localised documents).

**Prerequisites**

* Test for the existence of default element namespace.

**Test method**

* Check if there is a Title node in each Layer section.

**Reference(s)**: 
* [TG VS](README.md#ref_TG_VS), Chapter 4.2.3.3.4.1

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
Title <a name="Title"></a> | /WMS_Capabilities/Capability/Layer/Title
Layer <a name="Layer"></a> | /WMS_Capabilities/Capability/Layer
