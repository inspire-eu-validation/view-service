# Data visualization legend layer

**Purpose**: Legend is required for explaining the data visualization used for each layer. If the legend contains language-specific elements, localized legends shall be made available in each localized capabilities document.

**Prerequisites**

* [Schema validation](http://inspire.ec.europa.eu/id/ats/view-service/3.11/WMTS/schema-validation)
* [Layer style name](http://inspire.ec.europa.eu/id/ats/view-service/3.11/WMTS/layer-style-name)

**Test method**
For each Layer element:

* Check that for each [Style element](#Style):
  * There exists a non-empty [href attribute](#href). Let the value of the attibute be ```href```.
  * Retrieve the resource at the URL in ```href```. If the download is successful and a non-empty image file returned:
    * If the [Format](#format) equals 'image/gif' or 'image/png':
      * the downloaded resource must be a valid image of these image formats correspondingly. If it is, pass the test. If not, fail the test for this Style.
    * Otherwise, pass the test for this Style.
  * Otherwise, fail the test for this Style.

**Reference(s)**

* [TG VS](http://inspire.ec.europa.eu/id/ats/view-service/3.11/WMTS/README#ref_TG_VS), chapter 5.2.3.3.4.9, Requirement 91

**Test type**: Automated

**Notes**

* Note that it's generally not required for the validator to recognize the image formats of the downloaded legend files in order to pass the test.

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/view-service/3.11/WMTS/README#namespaces).

Abbreviation                                               |  XPath expression (relative to Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Style <a name="Style"></a> | ./wmts:Contents/wmts:Layer/wmts:Style
HREF attribute <a name="href"></a> | /wmts:Contents/wmts:Layer/wmts:Style/wmts:LegendURL[@xlink:href]
Format <a name="format"></a> | ./wmts:Contents/wmts:Layer/wmts:Style/wmts:LegendURL[@format]
