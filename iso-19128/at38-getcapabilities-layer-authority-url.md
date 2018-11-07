# Layer Authority URL

**Purpose**: Test that AuthorityURL and Identifier elements are used.

**Prerequisites**

**Test method**

* Send a getCapabilities request to the service endpoint. Into the response:

  * For each wms:Layer parent element:

    * Check if the [AuthorityURL](#AuthorityURL) element is given.
    * Check if the identifier of the authority is included in the "name" attribute of the element and the explanatory URL is given as an [OnlineResource](#OnlineResource) within AuthorityURL element.

    * Check if each subsidary layer has an [Identifier](#Identifier) element with an "authority" attribute matching with the AuthorityURL name declared in the parent layer or in the layer itself. The Identifier element must contain a unique identifier.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.4.5, Requirement 38

**Test type**: Automated

**Notes**

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
AuthorityURL <a name="AuthorityURL"></a> | wms:Capability/wms:Layer/AuthorityURL
OnlineResource <a name="OnlineResource"></a> | wms:Capability/wms:Layer/AuthorityURL/OnlineResource
Identifier <a name="Identifier"></a> | wms:Capability/*/wms:Layer/wms:Identifier