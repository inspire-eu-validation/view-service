# A.10.IR13.coupled.resource.node

**Purpose**: Coupled Resource shall be mapped to the elements of the Layer elements of the service capabilities. If linkage to the data sets or series on which the service operates are available, then the linkage to these resources shall be provided as stated by the INSPIRE Metadata Technical Guidance INS MDTG.

**Prerequisites**

* Test for the existence of default element namespace.

**Test method**

* Check if there is a MetadataURL node for each layer.
* If yes, check if the href in the OnlineResource node of the MetadataURL section is a valid link.


**Reference(s)**:
* [TG VS](README.md#ref_TG_VS), Chapter 4.2.3.3.1.5

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
MetadataURL <a name="MetadataURL"></a>   | /WMS_Capabilities/Capability/Layer/MetadataURL
OnlineResource/@xlink:href <a name="OnlineResource/@xlink:href"></a>   | /WMS_Capabilities/Capability/Layer/MetadataURL/Format/OnlineResource/@xlink:href
xlink | http://www.w3.org/1999/xlink
