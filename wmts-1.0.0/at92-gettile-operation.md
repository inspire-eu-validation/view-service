# GetTile Operation

**Purpose**: Test that the WMTS GetTile operation implements all the parameters according to the Commission Regulation (EC) No 976/2009.

**Prerequisites**

**Test method**

* The mandatory parameters for the GetTile operation are:
    * SERVICE=WMTS
    * REQUEST=GetTile
    * VERSION=1.0.0
    * LAYER
    * STYLE
    * FORMAT
    * TILEMATRIXSET
    * TILEMATRIX
    * TILECOL
    * TILEROW

    (The non-fixed values are taken from the capabilities document)

* Send a GetTile request with all the mandatory parameters.
  
  * Check that a valid non-empty response is provided. 

* For each parameter,

  * Send a GetTile request with all the mandatory parameters except the checked parameter.

  * Check that the response is not valid.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 5.2.3.3.4.9, Requirement 91
* [IR NS](./README.md#ref_IR_NS)

**Test type**: Automated

**Notes**

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------