# Data visualization legend layer

**Purpose**: Legend is required for explaining the data visualization used for each layer. If the legend contains language-specific elements, localized legends shall be made available in each localized capabilities document.

**Prerequisites**

* [Schema validation](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/schema-validation)
* [Layer style name](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/layer-style-name)

**Test method**
For each [Layer](#Layer) element provided by the service according to it's Service Metadata:

* Check that for each [Style element](#Style):
  * There exists a non-empty [href attribute](#href). Let the value of the attibute be ```href```.
  * Retrieve the resource at the URL in ```href```. If the download is successful and a non-empty image file returned:
    * If the [Format](#format) equals 'image/gif' or 'image/png':
      * the downloaded resource must be a valid image of these image formats correspondingly. If it is, pass the test. If not, fail the test for this Style.
    * Otherwise, pass the test for this Style.
  * Otherwise, fail the test for this Style.

**Reference(s)**

* [TG VS](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/README#ref_TG_VS), chapter 4.2.3.3.4.8, Requirement 45
* [TG VS](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/README#ref_TG_VS), chapter 4.2.3.3.4.8, Requirement 47
* [TG VS](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/README#ref_TG_VS), chapter 5.2.3.3.4.9, Requirement 91

**Test type**: Automated

**Notes**

* Note that it's generally not required for the validator to recognize the image formats of the downloaded legend files in order to pass the test.

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/README#namespaces).

Abbreviation                                     |  XPath expression												|  Parameter  value
------------------------------------------------ | ---------------------------------------------------------------	| ---------------------------------------------------------------
Layer <a name="Layer"></a> | /wms:WMS_Capabilities/wms:Capability/wms:Layer | ISO 19128
						   | /wmts:Capabilities/wmts:Contents/wmts:Layer | WMTS 1.0.0
Style <a name="Style"></a> | /WMS_Capabilities/Capability/Layer/Style | ISO 19128
						   | /wmts:Capabilities/wmts:Contents/wmts:Layer/wmts:Style | WMTS 1.0.0
href attribute <a name="href"></a> | ./wms:Style/wms:LegendURL/wms:OnlineResource[@xlink:href] | ISO 19128
								   | ./wmts:Style/wmts:LegendURL[@xlink:href] | WMTS 1.0.0
Format <a name="format"></a> | ./wms:Style/wms:LegendURL/wms:Format | ISO 19128
							 | ./wmts:Style/wmts:LegendURL[@format] | WMTS 1.0.0
