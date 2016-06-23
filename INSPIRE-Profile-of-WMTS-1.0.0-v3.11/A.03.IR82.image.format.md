# A.03.IR82.image.format

**Purpose**: To ensure that tiles for all layers provided by this service are made available in either PNG or GIF format (without LZW compression). The aim is to support clients capable of handling only a small set of different image formats, and to be able to use the same image basic formats with all INSPIRE services.

**Prerequisites**

* Test for the schema validity of the ServiceMetadata document has been passed.

**Test method**

For each [Layer element](#layer) provided by the service according to it's Service Metadata:
* Check that there is at least one [Format](#format) element either with content "image/png" or "image/gif".
* Make a GetTile request for the layer using a maximum allowed bounding box and either "image/png" or "image/gif" format and check that the returned image is encoded in the requested format.

**Reference(s)**: [TG VS](README.md#ref_TG_VS), Chapter 5.2.3.3.2.2

**Test type**: Automated

**Notes**


## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
Layer <a name="layer"></a> | /wmts:Capabilities/wmts:Contents/wmts:Layer
Format <a name="format"></a> | /wmts:Capabilities/wmts:Contents/wmts:Layer/wmts:Format
