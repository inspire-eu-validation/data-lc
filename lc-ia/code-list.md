# Code lists

**Purpose**: Verify that code lists extensions can be accessed.

**Prerequisites**

**Test method**

* Verify that any code list extensions are publicly accessible via HTTP, i.e. inspect extensible code list values property elements. If a reference (@xlink:href) has a value that does not start with http://inspire.ec.europa.eu/codelist/, verify that a HTTP GET request to the URI retrieves a document. Otherwise report [brokenLink](#brokenLink).

This data theme currently has the following empty code list:

* [LandCoverClassValue](#LandCoverClassValue): http://inspire.ec.europa.eu/codelist/LandCoverClassValue


**Reference(s)**: 

* [TG DS Template](./README.md#ref_TG_DS_tmpl) IR requirement Article 6 (3)

**Test type**: Automated

**Notes**

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
brokenLink <a name="brokenLink"/>  |  XML document '$filename', $featureType '$gmlid': The property '$propertyName' has a value '$value' that cannot be retrieved using HTTP. Every code list value must be made available in an online registry. 

## Contextual XPath references

The namespace prefixes used as described in [README](./README.md#namespaces).

Abbreviation                                               |  XPath expression      |Multiplicity   |Voidable
---------------------------------------------------------- | -----------------------|---------------|---------------------------------
LandCoverClassValue <a name="LandCoverClassValue"></a> | //schema-element(lcv:LandCoverUnit)/lcv:landCoverObservation/lcv:LandCoverObservation/lcv:class/@xlink:href <br> //schema-element(lcv:LandCoverDataset)/lcv:member/lcv:LandCoverUnit/lcv:landCoverObservation/lcv:LandCoverObservation/lcv:class/@xlink:href | 1 | No
" | //schema-element(lcv:LandCoverUnit)/lcv:landCoverObservation/lcv:LandCoverObservation/lcv:mosaic/lcv:LandCoverValue/lcv:class/@xlink:href <br> //schema-element(lcv:LandCoverDataset)/lcv:member/lcv:LandCoverUnit/lcv:landCoverObservation/lcv:LandCoverObservation/lcv:mosaic/lcv:LandCoverValue/lcv:class/@xlink:href | 1 (1..\* for the parent, lcv:mosaic) | No
