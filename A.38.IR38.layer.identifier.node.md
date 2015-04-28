# A.38.IR38.layer.identifier.node

**Purpose**: To be able to map the concept of a responsible body/codeSpace and local identifier/code to ISO 19128), AuthorityURL and Identifier elements shall be used. The authority name and explanatory URL shall be defined in a separate AuthorityURL element, which may be defined once and inherited by subsidiary layers. Identifiers themselves are not inherited.

**Prerequisites**

* Test for the existence of default element namespace.

**Test method**

* Check if there is a Identifier node in each Layer section other than layer without Name element formed from daughters and each Identifier node has been declared in an AuthorityURL node of the layer itself or its parent layer by heritage.

**Reference(s)**: 
* [TG VS](README.md#ref_TG_VS), Chapter 4.2.3.3.4.5
* IR Annex III, Part A, Chapter 2.2.4

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
Identifier <a name="Identifier"></a>   | /WMS_Capabilities/Capability/Layer/Identifier
Layer <a name="Layer"></a>   | /WMS_Capabilities/Capability/Layer
@authority <a name="@authority"></a>   | /WMS_Capabilities/Capability/Layer/Identifier/@authority
