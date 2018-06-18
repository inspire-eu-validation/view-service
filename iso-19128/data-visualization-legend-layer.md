# Data visualization legend layer

**Purpose**: Legend is required for explaining the data visualization used for each layer. If the legend contains language-specific elements, localized legends shall be made available in each localized capabilities document.

**Prerequisites**

* [Schema validation](http://inspire.ec.europa.eu/id/ats/view-service/3.11/ISO-19128/schema-validation)
* [Layer style name](http://inspire.ec.europa.eu/id/ats/view-service/3.11/ISO-19128/layer-style-name)

**Test method**
For each [Layer](#Layer) element provided by the service according to it's Service Metadata:

* Check that for each [Style element](#Style):
  * There exists a non-empty [href attribute](#href). Let the value of the attibute be ```href```.
  * Retrieve the resource at the URL in ```href```. If the download is successful and a non-empty image file returned:
    * If the [Format](#format) equals 'image/gif' or 'image/png':
      * the downloaded resource must be a valid image of these image formats correspondingly. If it is, pass the test for this Style.
    * Otherwise, pass the test for this Style.
  * Otherwise, fail the test for this Style.

**Reference(s)**

* [TG VS](http://inspire.ec.europa.eu/id/ats/view-service/3.11/ISO-19128/README#ref_TG_VS), chapter 4.2.3.3.4.8, Requirement 45, 47

**Test type**: Automated

**Notes**

* Note that it's generally not required for the validator to recognize the image formats of the downloaded legend files in order to pass the test.

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/view-service/3.11/ISO-19128/README#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Layer <a name="Layer"></a> | ./wms:Capability/wms:Layer
Style <a name="Style"></a> | ./wms:Capability/wms:Layer/wms:Style/
HREF attribute <a name="href"></a> | ./wms:Capability/wms:Layer/wms:Style/wms:LegendURL/wms:OnlineResource[@xlink:href]
Format <a name="format"></a> | ./wms:Capability/wms:Layer/wms:Style/wms:LegendURL/wms:Format
