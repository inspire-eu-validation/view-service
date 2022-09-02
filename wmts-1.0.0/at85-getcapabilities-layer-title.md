# Layer Title

**Purpose**: Test that Layer Title is mapped to Title element for each layer, and for each harmonised layer according to [IR IOP](./README.md#ref_IR_IOP), the title is mapped to the harmonised title defined by [IR IOP](./README.md#ref_IR_IOP).

**Prerequisites**

**Test method**

* Send a getCapabilities request to the service endpoint. Into the response:

  * For each [Layer](#layer) element:

    If a [Title](#title) element is provided:

    * Check that it has a non-empty value.
  
  *  Check manually that for each harmonised layer according to [IR IOP](./README.md#ref_IR_IOP), the title is mapped to the harmonised title defined by [IR IOP](./README.md#ref_IR_IOP).

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 5.2.3.3.4.1, Requirement 85
* [IR IOP](./README.md#ref_IR_IOP), Article 14

**Test type**: Automated + Manual

**Notes**

The multiplicity of the Title element is 0 or 1 for each layer.

The harmonished title of the layer shall be subject to multilingualism.

The validation of the correctness of the translated title is not done due to it's complexity and the controversy over the usefulness of the harmonised layer titles.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Layer <a name="layer"></a> | Contents/Layer
Title <a name="title"></a> | Contents/Layer/ows:Title
