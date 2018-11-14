# Layer Metadata

**Purpose**: Test that a Metadata element is provided for each Layer pointing to the metadata document.

**Prerequisites**

**Test method**

* Send a getCapabilities request to the service endpoint. Into the response:

    * For each Layer element:

      * Check that a [Metadata](#metadata) element is provided.

      * Check that this element is populated with an URL allowing access to an unambiguous metadata record. The URL must be:
        * A HTTP/GET call to the GetRecordById operation of the Discovery service using the identifier of the metadata document.
        * A direct link to the metadata document.

      * Check that a valid response is retuned calling to the provided URL.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 5.2.3.1, Requirement 79

**Test type**: Automated

**Notes**

The multiplicity of this element is 1 in each Layer element.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Metadata <a name="metadata"></a> | Layer/ows:Metadata