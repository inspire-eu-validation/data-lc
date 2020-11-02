# Constraints

**Purpose**: Verify that the features provided in the dataset adhere to the constraints specified in the INSPIRE application schema.

**Prerequisites**

**Test method**

The following check is performed for every feature in the dataset.

* **rangeSetIsKindOfLandCoverClassValue**: Check manually that the values in the range set are restricted to Integer. (OCL: inv:rangeSet->forAll(v | v.oclIsKindOf(LandCoverNomenclature::LandCoverClassValue))).


**Reference(s)**: 

* [TG DS Template](./README.md#ref_TG_DS_tmpl) IR requirement Article 4 (2)
* [TG DS-LC](./README.md#ref_TG_DS_LC) 5.6.2.1.1.

**Test type**: Manual

**Notes** 

See also the [theme-specific requirement](./specific-req.md).

Only the equivalent of the information classValue found in the Vector representation (i.e. the reference to a code list through the type LandCoverClassValue) is then supported by the raster representation of LC data (rangeSetIsKindOfLandCoverClassValue constraint). The rangeSet of the raster allows attaching a single classification code, resulting from a classification process, to each raster cell. These can be Corine codes, IGBP codes or other codes corresponding to a national, institutional or local nomenclature.
These restrictions are linked to the formats used to encode rectified grid coverages (as Geotiff) which only support one value per pixel.

Verify that the OCL constraints that are specified in the UML model of the application schema are met, i.e. validate features against the constraints. For unmet constraints report [constraintViolation](#constraintViolation).

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
constraintViolation <a name="constraintViolation"/>  |  XML document '$filename', $featureType '$gmlid': The constraint '$constraint' is violated.

## Contextual XPath references

The namespace prefixes used as described in [README](./README.md#namespaces).

Abbreviation                                               |  XPath expression                     |Multiplicity       |Voidable
---------------------------------------------------------- | ------------------------------------- | ------------------|----------
