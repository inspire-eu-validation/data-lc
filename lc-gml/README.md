# Conformance class: GML application schemas, Land Cover

Conformance class for the GML encoding of spatial objects specified in the INSPIRE GML application schema 'Land Cover'. This conformance class examines the data set against requirements associated with the GML application schema.

This conformance class is part of the [INSPIRE Data Specification on Land Cover](../README.md).

## Standardization target type

INSPIRE spatial data set encoded in GML, Land Cover features

## Dependencies

### Direct dependencies

A direct dependency is another conformance class whose requirements must be met by the GML documents, too.

| Specification | Conformance class | Parameters | 
| ------------- | ----------------- | ---------- |
| [TG DS Template](#ref_TG_DS_tmpl) | [INSPIRE GML application schemas](http://inspire.ec.europa.eu/id/ats/data/3.0rc3/schemas) | n/a |

### Indirect dependencies

n/a
 
## External document references

The following abbreviations are used in the test text for referring to external documents:

Abbreviation                     | Document name
-------------------------------- | --------------------------------------------------
TG DS-LC <a name="ref_TG_DS_LC"></a>   | [INSPIRE Data Specification on Land Cover – Technical Guidelines version 3.0](https://inspire.ec.europa.eu/documents/Data_Specifications/INSPIRE_DataSpecification_LC_v3.0.pdf)
TG DS Template <a name="ref_TG_DS_tmpl"></a>   | [INSPIRE Data Specification Template version 3.0rc3](http://inspire.jrc.ec.europa.eu/documents/Data_Specifications/INSPIRE_DataSpecification_Template_v3.0rc3.pdf)

## Test Cases

| Identifier                                                        | Status   | Test case in [TG DS-LC](#ref_TG_DS_LC)  |
| ----------------------------------------------------------------- | -------- | ------------ |
| [Basic test](./basic.md)  | ready for review  | A.1.1, (A.6.1)  |
| [Validation against INSPIRE official schema](./official-schema-validation.md)  | ready for review  | A.1.1, (A.6.1)  |

## XML namespace prefixes <a name="namespaces"></a>

The following prefixes are used to refer to the corresponding XML namespaces in all test descriptions:

Prefix         | Namespace
-------------- | -------------------------------------------------
lcn    	       | http://inspire.ec.europa.eu/schemas/lcn/4.0
lcr		 	   | http://inspire.ec.europa.eu/schemas/lcr/4.0
lcv		 	   | http://inspire.ec.europa.eu/schemas/lcv/4.0
