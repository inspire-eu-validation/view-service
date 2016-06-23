# A.05.IR85.layer.title

**Purpose**: The layer title must reflect the layer content in a language and terms the users' are expected to understand.

**Prerequisites**

* Test for the schema validity of the ServiceMetadata document has been passed.

**Test method**

For each [Layer element](#layer) provided by the service according to it's Service Metadata:

* Check that the [Title element](#title) is a non-empty character string. If so, pass the test.

**Reference(s)**: [IR IOP](README.md#ref_IR_IOP), [TG VS](README.md#ref_TG_VS), chapter 5.2.3.3.4.1

**Test type**: Automated

**Notes**

The validation of the correctness of the translated title is not done due to it's complexity and the controversy over the usefulness of the harmonised layer titles. If this is decided to be necessary, the procedure should be similar to one used in `A.04.layer.name.id`.

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
Layer <a name="layer"></a> | /wmts:Capabilities/wmts:Contents/wmts:Layer
Title <a name="title"></a> | /wmts:Capabilities/wmts:Contents/wmts:Layer/ows:Title
