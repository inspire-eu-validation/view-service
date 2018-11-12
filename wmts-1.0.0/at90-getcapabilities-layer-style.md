# Layer Style Title and Identifier

**Purpose**: Test that each style has a human-readable name mapped to Title element and a unique identifier mapped to Identifier element.

**Prerequisites**

**Test method**

* Send a getCapabilities request to the service endpoint. Into the response:

  * Check that the layer styles are mapped into the [Style](#style) element. 
  
  * For each wms:Style element:

    * Check if a human-readable name is mapped to the [Title](#title) element.
    * Check if the Unique Identifier is mapped to the [Identifier](#identifier) element.
      * Check if the [unique identifier](#identifier) is unique within the style elements of the layer.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 5.2.3.3.4.8, Requirement 90

**Test type**: Automated

**Notes**

The multiplicity of both elements is 1 in each style.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Title <a name="title"></a> | Contents/Layer/Style/ows:Title
Identifier <a name="identifier"></a> | Contents/Layer/Style/ows:Identifier
