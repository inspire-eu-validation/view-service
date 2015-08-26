# A.11.IR14.metadata.record.node

**Purpose**: Each of the elements shall be populated with a URL that allows access to an unambiguous metadata record. The URL shall be either an HTTP/GET call on the GetRecordById operation of the Discovery Service or a direct link to the ISO 19139 metadata document.

**Prerequisites**

* Test for the existence of default element namespace.

**Test method**

* Then check if there is a MetadataURL node for each layer.
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
