# Layer Name

**Purpose**: Test that in each layer, the layer name is mapped into the Name element.

**Prerequisites**

**Test method**

* Send a getCapabilities request to the service endpoint. Into the response:

  * For each wms:Layer element:

    * Check if is provided a [Layer Name](#layerName) element and it is a non-empty free text.

    * Check if harmonished name of the layer comply with the Layer requirements of the [IR IOP, Article 14]. 
      * [Layer Name](#layerName) element value must start by one of the themes name:
        * GN.GeographicalNames
        * AU.AdministrativeUnit
        * AD.Address
        * CP.CadastralParcel
        * TN.RoadTransportNetwork.RoadArea
        * HY.Network
        * PS.ProtectedSite



**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.4.6, Requirement 39
* [IR IOP](./README.md#ref_IR_IOP), Article 14

**Test type**: Automated

**Notes**

The multiplicity of this element is 1 for each layer.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Layer Name <a name="layerName"></a> | wms:Capability/*/wms:Layer/wms:Name
