# Layer Keywords

**Purpose**: Test that a list of keywords is provided into a Keywords element in each layer.

**Prerequisites**

**Test method**

* Send a getCapabilities request to the service endpoint. Into the response:

  * For each [Layer](#layer) element:

    If a [Keywords](#keywords) element is provided,

    * Check that [Keywords](#keywords) element contains at least one [Keyword](#keyword) element and it has a non-empty value.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 5.2.3.3.4.3, Requirement 87

**Test type**: Automated

**Notes**

The multiplicity of the Keywords element is 0 or more for each layer.

The multiplicity of Keyword elements is 1 or more within each Keywords element.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Layer <a name="layer"></a> | Contents/Layer
Keywords <a name="keywords"></a> | Contents/Layer/ows:Keywords
Keyword <a name="keyword"></a> | Contents/Layer/ows:Keywords/ows:Keyword