# Layer Style Identifier and Title

**Purpose**: Test that each style has a unique identifier mapped to Identifier element and if a human-readable name is included, it is mapped to Title element.

**Prerequisites**

**Test method**

* Send a getCapabilities request to the service endpoint. Into the response:

  * Check that the layer styles are mapped into the [Style](#style) element. 
  
  * For each [Style](#style) element:

    * Check if the Unique Identifier is mapped to the [Identifier](#identifier) element.
      * Check if the [unique identifier](#identifier) is unique within the style elements of the layer.

    If a human-readable name is mapped to [Title](#title) element:
      * Check if [Title](#title) element has a non-empty value.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 5.2.3.3.4.8, Requirement 90

**Test type**: Automated

**Notes**

The multiplicity of the Identifier element is 1 in each style.
The multiplicity of the Title element is 0 or more in each style.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Style <a name="style"></a> | Contents/Layer/Style
Title <a name="title"></a> | Contents/Layer/Style/ows:Title
Identifier <a name="identifier"></a> | Contents/Layer/Style/ows:Identifier
