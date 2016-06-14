# A.32.IR38.layer.identifier.node

**Purpose**: To be able to map the concept of a responsible body/codeSpace and local identifier/code to ISO 19128), AuthorityURL and Identifier elements shall be used. The authority name and explanatory URL shall be defined in a separate AuthorityURL element, which may be defined once and inherited by subsidiary layers. Identifiers themselves are not inherited.

**Prerequisites**

* Test for the existence of default element namespace.

**Test method**

* Check if there is a [Identifier](#Identifier) with attribute [@authority](#authority) node in each [Layer](#Layer) section other than layer without [Name](#Name) element formed from daughters
* Check whether each [Identifier](#Identifier) node has been declared in an [AuthorityURL](#AuthorityURL) node of the layer itself or its parent layer by heritage by comparing the [@authority](#authority) attribute of the [Identifier](#Identifier) element with the [@name](#AuthorityURLName) attribute of the [AuthorityURL](#AuthorityURL) element.

**Reference(s)**:
* [TG VS](README.md#ref_TG_VS), Chapter 4.2.3.3.4.5
* IR Annex III, Part A, Chapter 2.2.4

**Notes**
* Group layers with a name will fail the test. A TG update is required to support group layers properly.

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
Layer <a name="Layer"></a>   | /wms:WMS_Capabilities/wms:Capability/wms:Layer
Name <a name="Name"></a>   | /wms:WMS_Capabilities/wms:Capability/wms:Layer/wms:Name
Identifier <a name="Identifier"></a>   | /wms:WMS_Capabilities/wms:Capability/wms:Layer/Identifier
@authority <a name="authority"></a>   | /wms:WMS_Capabilities/wms:Capability/wms:Layer/Identifier[@authority]
AuthorityURL <a name="AuthorityURL"></a>   | /wms:WMS_Capabilities/wms:Capability/wms:Layer/AuthorityURL
@name <a name="AuthorityURLName"></a>   | /wms:WMS_Capabilities/wms:Capability/wms:Layer/AuthorityURL[@name]
