# Constraints

**Purpose**: Verify that the features provided in the dataset adhere to the constraints specified in the INSPIRE application schema.

**Prerequisites**

**Test method**

The following check is performed for every feature in the dataset.

* Check that the [embedded description](#embedded) OR the [external description](#external) is provided.


**Reference(s)**: 

* [TG DS Template](./README.md#ref_TG_DS_tmpl) IR requirement Article 4 (2)
* [TG DS-LC](./README.md#ref_TG_DS_LC) 5.4.2.1.1.

**Test type**: Automated

**Notes** 

Verify that the OCL constraints that are specified in the UML model of the application schema are met, i.e. validate features against the constraints. For unmet constraints report [constraintViolation](#constraintViolation).

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
constraintViolation <a name="constraintViolation"/>  |  XML document '$filename', $featureType '$gmlid': The constraint '$constraint' is violated.

## Contextual XPath references

The namespace prefixes used as described in [README](./README.md#namespaces).

Abbreviation                   |  XPath expression                 |Multiplicity       |Voidable
------------------------------ | --------------------------------- | ------------------|----------
external description <a name="external"></a> | //schema-element(lcv:LandCoverDataset)/lcv:nomenclatureDocumentation/lcn:LandCoverNomenclature/lcn:externalDescription | 0..\* | Yes
TO BE COMPLETED