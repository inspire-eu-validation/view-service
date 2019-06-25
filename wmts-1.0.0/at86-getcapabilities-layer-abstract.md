# Layer Abstract

**Purpose**: Test that if an Abstract element is provided, it is not empty and it is written in the language of the Capabilities document.

**Prerequisites**

**Test method**

* Send a getCapabilities request to the service endpoint. Into the response:

  * For each [Layer](#layer) element:

    If an [Abstract](#abstract) element is provided:

    * Check that it has a non-empty value.

    * Check manually that the language of the [Abstract](#abstract) element content matches with the language of the Capabilities document.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 5.2.3.3.4.2, Requirement 86

**Test type**: Automated/Manual

**Notes**

The multiplicity of the Abstract element is 0 or 1 for each layer.

The layer abstract shall be subject to multilingalism.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Layer <a name="layer"></a> | Contents/Layer
Abstract <a name="abstract"></a> | Contents/Layer/ows:Abstract