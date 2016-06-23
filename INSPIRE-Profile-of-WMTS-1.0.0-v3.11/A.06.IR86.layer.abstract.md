# A.06.IR86.layer.abstract

**Purpose**: The layer must be described in a language and terms the users' are expected to understand.

**Prerequisites**

* Test for the schema validity of the ServiceMetadata document has been passed.

**Test method**

For each [Layer element](#layer) provided by the service according to it's Service Metadata:

* Check that the [Abstract element](#abstract) is a non-empty character string. If so, pass the test.

**Reference(s)**: [IR IOP](README.md#ref_IR_IOP), [TG VS](README.md#ref_TG_VS), chapter 5.2.3.3.4.2

**Test type**: Automated

**Notes**

This a the description of the layer (a portrayal), not the same thing as the metadata record of the dataset which the layer is visualising.


## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
Layer <a name="layer"></a> | /wmts:Capabilities/wmts:Contents/wmts:Layer
Abstract <a name="abstract"></a> | /wmts:Capabilities/wmts:Contents/wmts:Layer/ows:Abstract
