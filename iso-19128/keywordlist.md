# Keyword list

**Purpose**: Keywords shall be mapped to the wms:KeywordList element. At least one keyword provided shall be from the "Classification of spatial data Services" (Part D.4 from INS MD) in case of spatial data services. If a vocabulary is mapped, it shall be done in the 'vocabulary' attribute of the Keyword element.

**Prerequisites**

* [Schema validation](./schema-validation.md)
* [Keyword node](./keyword-node.md)

**Test method**

* Check, in case of spatial data services, if it is provided at least one keyword from the "Classification of spatial data Services" (Part D.4 from [INS MD](./README.md#ref_INS_MD)).
* Check, in case additional keywords are provided, if they are mapped with a [KeywordList](#KeywordList) element.
* Check if the referenced vocabulary is mapped to the 'vocabulary' attribute of the [Keyword](#Keyword) element.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.4.3, Requirement 17,35
* [INS MD](./README.md#ref_INS_MD), Part D.4 Classification of spatial Data Services

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
KeywordList <a name="KeywordList"></a> | ./wms:Capability/wms:Service/wms:KeywordList
Keyword <a name="Keyword"></a> | ./wms:Capability/wms:Service/wms:KeywordList/wms:Keyword
