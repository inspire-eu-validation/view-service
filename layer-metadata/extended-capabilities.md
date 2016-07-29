# Extended Capabilities

**Purpose**: The metadata response parameters shall be provided through the service Capabilities. These capabilities are mandatory and defined when a WMS or WMTS is set up. They consist of service information, supported operations and parameters values. INSPIRE requires additional metadata (extended capabilities).

**Prerequisites**

* [Schema validation](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/schema-validation)

**Test method**

* Check that the [ExtendedCapabilities](#extendedCapabilities) exist. If yes:
  * Validate the [ExtendedCapabilities](#ExtendedCapabilities) element and it's children according to the XML Schema definition for the INSPIRE Extended Capabilities as defined in the http://inspire.ec.europa.eu/schemas/inspire_vs/1.0/inspire_vs.xsd
  * If the validation passes, pass the test.
* If no ExtendedCapabilities were found or validation fails, fail the test.

**Reference (s)**: 

* [TG VS](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/README#ref_TG_VS), Chapter 4.2.3.3.1, Requirement 6
* [TG VS](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/README#ref_TG_VS), Chapter 5.2.3.3.1

**Test type**: Automated

**Notes**


## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/README#namespaces).

Abbreviation                                     |  XPath expression												|  Parameter  value
------------------------------------------------ | ---------------------------------------------------------------	| ---------------------------------------------------------------
ExtendedCapabilities <a name="extendedCapabilities"></a>   | /wms:WMS_Capabilities/wms:Capability/inspire_vs:ExtendedCapabilities | ISO 19128
                                                           | /wmts:Capabilities/ows:OperationsMetadata/inspire_vs_ows11:ExtendedCapabilities | ISO 19128
