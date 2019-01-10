# Layer Authority URL

**Purpose**: Test that AuthorityURL and Identifier elements are used.

**Prerequisites**

**Test method**

* Send a getCapabilities request to the service endpoint. Into the response:

* For each [AuthorityURL](#AuthorityURL) element

    * Check that the "name" attribute exists and the explanatory URL is given as an [OnlineResource](#OnlineResource) within the AuthorityURL element.

* For each [Layer](#layer) element:

    * For each [AuthorityURL](#AuthorityURL) element given in the node itself or in the parents layers elements.

        * Check that authority name has not be defined previously.

    * Check that the "authority" attribute of [Identifier](#Identifier) element matches with the [AuthorityURL](#AuthorityURL) name declared in the parents layers or in the layer itself.

* For each [Identifier](#Identifier) element:
    
    * Check that the [Identifier](#Identifier) element is unique for its authority.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.4.5, Requirement 38

**Test type**: Automated

**Notes**

The multiplicity of [AuthorityURL](#AuthorityURL) is 0 or more.

The multiplicity of [Identifier](#Identifier) is 0 or more.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Layer <a name="layer"></a> | wms:Capability/*/wms:Layer
AuthorityURL <a name="AuthorityURL"></a> | wms:Capability/*/wms:Layer/AuthorityURL
OnlineResource <a name="OnlineResource"></a> | wms:Capability/*/wms:Layer/AuthorityURL/OnlineResource
Identifier <a name="Identifier"></a> | wms:Capability/*/wms:Layer/wms:Identifier