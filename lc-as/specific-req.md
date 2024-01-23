# Land Cover theme-specific requirement

**Purpose**: Verify that, if an [externalDescription](#external) attribute is provided for a LandCoverNomenclature data type, the referenced online description shall define, for each class, at least a code, a name, a definition and a RGB value to be used for portrayal. If the online description describes the nomenclature for a LandCoverGridCoverage object, an integer grid code shall also be provided for each class. This code shall be used in the range of the LandCoverGridCoverage to represent the corresponding class.

**Prerequisites**

**Test method**

If an [externalDescription](#external) attribute is provided for a LandCoverNomenclature data type, check manually that the referenced online description defines, for each class, at least a code, a name, a definition and a RGB value to be used for portrayal. If the online description describes the nomenclature for a LandCoverGridCoverage object, an integer grid code shall also be provided for each class. This code shall be used in the range of the LandCoverGridCoverage to represent the corresponding class.


**Reference(s)**: 

* [TG DS Template](./README.md#ref_TG_DS_tmpl) IR requirement Article 12 (1)
* [TG DS-LC](./README.md#ref_TG_DS_LC) 5.4.1.2.1.

**Test type**: Manual

**Notes** 


## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------

## Contextual XPath references

The namespace prefixes used as described in [README](./README.md#namespaces).

Abbreviation                   |  XPath expression                 |Multiplicity       |Voidable
------------------------------ | --------------------------------- | ------------------|----------
external description <a name="external"></a> | //schema-element(lcv:LandCoverDataset)/lcv:nomenclatureDocumentation/lcn:LandCoverNomenclature/lcn:externalDescription | 0..\* | Yes
" | //schema-element(lcr:LandCoverGridCoverage)/lcr:nomenclatureDocumentation/lcn:LandCoverNomenclature/lcn:externalDescription | 0..\* | Yes
