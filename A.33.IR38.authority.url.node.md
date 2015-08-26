# A.33.IR38.authority.url.node

**Purpose**: The INS MD Regulation defines a Unique Resource Identifier as a value uniquely identifying an object within a namespace. The code property shall be specified at a minimum, and a codeSpace (namespace) property may be provided.

**Prerequisites**

* Test for the existence of default element namespace.

**Test method**

* Check if there is a AuthorityURL node in each Layer section.

**Reference(s)**:
* [TG VS](README.md#ref_TG_VS), Chapter 4.2.3.3.4.5
* IR Annex III, Part A, Chapter 2.2.4

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
AuthorityUrl <a name="AuthorityUrl"></a> | /WMS_Capabilities/Capability/Layer/AuthorityUrl
Layer <a name="Layer"></a> | /WMS_Capabilities/Capability/Layer
