# Layer Metadata Element

**Purpose**: Test that a Metadata element is provided for each Layer pointing to the metadata document.

**Prerequisites**

**Test method**

* Send a getCapabilities request to the service endpoint. Into the response:

    * For each Layer element:

      If exists a [Metadata](#metadata) element:

      * Check that this element is populated in the "xlink:href" attribute with an URL allowing access to an unambiguous metadata record. The URL must be:
        * A HTTP/GET call to the GetRecordById operation of the Discovery service using the identifier of the metadata document.
        * A direct link to the metadata document.

      * Check that a valid response is returned calling to the provided URL.
        
        In case of a csw:GetRecordByIdResponse document, 
        * Check that exists a gmd:MD_Metadata child element.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 5.2.3.1, Requirement 79

**Test type**: Automated

**Notes**

The multiplicity of Metadata element is 0 or more in each Layer element.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Metadata <a name="metadata"></a> | Contents/Layer/ows:Metadata