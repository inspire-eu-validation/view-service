#A.08.IR90.layer.style

**Purpose**: Each layer must include at least one style according to the WMTS specification. To be easily identifiable each style must include a human-readable name and a unique identifier for that style to be used in requests.

**Prerequisites**

* Test for the schema validity of the ServiceMetadata document has been passed.

**Test method**

For each [Layer element](#layer) provided by the service according to it's Service Metadata:
* For each [Style element](#style) of the layer:
  * Check that the [Title element](#title) exists and is a non-empty character string.
* Check that the character strings of the [Identifier elements](#identifier) for each [Style elements](#style) are unique within the style.

**Reference(s)**: [TG VS](README.md#ref_TG_VS), chapter 5.2.3.3.4.8

**Test type**: Automated

**Notes**

The WMTS schema validity requires at least one [Style element](#style) per [Layer element](#layer) and exactly one
[Identifier element](#identifier) per [Style element](#style), so it's not necessary to add additional checks for them.

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
Layer <a name="layer"></a> | /wmts:Capabilities/wmts:Contents/wmts:Layer
Style <a name="style"></a> | /wmts:Capabilities/wmts:Contents/wmts:Layer/wmts:Style
Title <a name="title"></a> | /wmts:Capabilities/wmts:Contents/wmts:Layer/wmts:Style/ows:Title
Identifier <a name="identifier"></a> | /wmts:Capabilities/wmts:Contents/wmts:Layer/wmts:Style/ows:Identifier
