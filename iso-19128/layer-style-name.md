# Layer style name

**Purpose**: Each layer must include at least one style according to the both the ISO 19128 specification. To be easily identifiable each style must include a human-readable name and a unique identifier for that style to be used in requests.

**Prerequisites**

* [Schema validation](http://inspire.ec.europa.eu/id/ats/view-service/3.11/ISO-19128/schema-validation)

**Test method**

For each Layer element provided:
* For each Style element of the layer:
  * Check that the [Title element](#Title) exists and is a non-empty character string.
* Check that the character strings of the [Identifier elements](#Identifier) for each Style element are unique within the style.

**Reference(s)**:
* [TG VS](http://inspire.ec.europa.eu/id/ats/view-service/3.11/ISO-19128/README#ref_TG_VS) 4.2.3.3.4.8, Requirement 41, 46

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/view-service/3.11/ISO-19128/README#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Title <a name="Title"></a> | ./wms:Capability/wms:Layer/wms:Style/wms:Title
Identifier <a name="Identifier"></a> | ./wms:Capability/wms:Layer/wms:Style/wms:Name
