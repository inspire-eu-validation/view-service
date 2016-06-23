#A.08.IR91.layer.legend

**Purpose**: Each layer must include at least one style according to the WMTS specification. Legend is necessary for each describing the colors and symbols used in each style.  

**Prerequisites**

* Test [A.08.IR90.layer.style](A.08.IR90.layer.style.md) has been passed.

**Test method**

For each [Layer element](#layer) provided by the service according to it's Service Metadata:
* For each [Style element](#style) of the layer:
  * Check that the at least one [LegendURL element](#legendURL) exists and it has an [href attribute](#href_attr) containing a valid HTTP URL which resolves to a resource accessible through the Internet

**Reference(s)**: [TG VS](README.md#ref_TG_VS), chapter 5.2.3.3.4.9, [INSPIRE Directive](README.md#ref_INSPIRE), Article 11

**Test type**: Automated

**Notes**

The INSPIRE directive text lists displaying the legend information as part of the minimum set of required functionalities for a view service (Article 11):

> b) view services making it possible, as a minimum, to display,
  navigate, zoom in/out, pan, or overlay viewable spatial data
  sets and to display legend information and any relevant
  content of metadata;

As there are no requirements in the TG about the use of the [format attribute](#format_attr), nor about the acceptable
image formats to use for legend graphics, it's not possible check if the resolved legend resource is a valid image.

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
Layer <a name="layer"></a> | /wmts:Capabilities/wmts:Contents/wmts:Layer
Style <a name="style"></a> | /wmts:Capabilities/wmts:Contents/wmts:Layer/wmts:Style
LegendURL <a name="legendURL"></a> | /wmts:Capabilities/wmts:Contents/wmts:Layer/wmts:Style/wmts:LegendURL
href attribute <a name="href_attr"></a> | /wmts:Capabilities/wmts:Contents/wmts:Layer/wmts:Style/wmts:LegendURL@xlink:href
format attribute <a name="format_attr"></a> | /wmts:Capabilities/wmts:Contents/wmts:Layer/wmts:Style/wmts:LegendURL@format
