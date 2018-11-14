# Layer Abstract

**Purpose**: Test that an Abstract element is provided for each layer describing it.

**Prerequisites**

**Test method**

* Send a getCapabilities request to the service endpoint. Into the response:

  * For each Layer element:

    * Check that it contains a [Abstract](#abstract) element and it has a non-empty value.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 5.2.3.3.4.2, Requirement 86

**Test type**: Automated

**Notes**

The multiplicity of this element is 1 for each layer.

The layer abstract shall be subject to multilingalism.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Abstract <a name="abstract"></a> | Contents/Layer/ows:Abstract