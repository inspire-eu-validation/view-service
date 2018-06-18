# Layer style name

**Purpose**: Each layer must include at least one style according to the both the ISO 19128 and WMTS specification. To be easily identifiable each style must include a human-readable name and a unique identifier for that style to be used in requests.

**Prerequisites**

* [Schema validation](http://inspire.ec.europa.eu/id/ats/view-service/3.11/WMTS/schema-validation)

**Test method**

For each Layer element provided:
* For each Style element of the layer:
  * Check that the [Title element](#Title) exists and is a non-empty character string.
* Check that the character strings of the [Identifier elements](#Identifier) for each [Style elements](#Style) are unique within the style.

**Reference(s)**:
* [TG VS](http://inspire.ec.europa.eu/id/ats/view-service/3.11/WMTS/README#ref_TG_VS) 5.2.3.3.4.8, Requirement 90

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/view-service/3.11/WMTS/README#namespaces).

Abbreviation                                               |  XPath expression (relative to Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Title <a name="Title"></a> | ./wmts:Contents/wmts:Layer/wmts:Style/wms:Title
Identifier <a name="Identifier"></a> | ./wmts:Contents/wmts:Layer/wmts:Style/wms:Name
