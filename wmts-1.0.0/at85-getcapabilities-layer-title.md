# Layer Resource Title

**Purpose**: Test that a Title element is provided for each layer with the harmonished title.

**Prerequisites**

**Test method**

* Send a getCapabilities request to the service endpoint. Into the response:

  * For each Layer element:

    * Check that it contains a [Title](#title) element and it is a non-empty free text.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 5.2.3.3.4.1, Requirement 85

**Test type**: Automated

**Notes**

The multiplicity of this element is 1 for each layer.

The harmonished title of the layer shall be subject to multilingualism.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Title <a name="title"></a> | Contents/Layer/ows:Title