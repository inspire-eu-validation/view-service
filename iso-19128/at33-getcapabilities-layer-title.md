# Layer Title

**Purpose**: Test that each layer element contains a Title element and, for each harmonised layer according to [IR IOP](./README.md#ref_IR_IOP), the title is mapped to the harmonised title defined by [IR IOP](./README.md#ref_IR_IOP).

**Prerequisites**

**Test method**

* Send a getCapabilities request to the service endpoint. Into the response:

  * For each [Layer](#layer) element:

    * Check that it contains exactly one [Title](#title) element and its value is not empty.
    * Check manually that for each harmonised layer according to [IR IOP](./README.md#ref_IR_IOP), the title is mapped to the harmonised title defined by [IR IOP](./README.md#ref_IR_IOP).

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.4.1, Requirement 33
* [IR IOP](./README.md#ref_IR_IOP), Article 14

**Test type**: Automated + Manual

**Notes**

The multiplicity of this element is 1 for each layer element.

Title element shall be subject to multilingualism, therefore, translations shall appear in each mono-lingual capabilities localised documents.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Layer <a name="layer"></a> | wms:Capability/*/wms:Layer
Title <a name="title"></a> | wms:Capability/*/wms:Layer/wms:Title
