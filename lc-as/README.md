# Conformance class: Application schema, Land Cover Nomenclature

Conformance class for the requirements associated with the application schema. 

To be able to test this conformance class, the encoding of the data set must be known, i.e. this is a parameterized conformance class. The XPath expressions used in this test suite assume that the GML encoding is used. If used with the GML encoding this conformance class has an indirect dependency to the conformance class "GML application schemas, Land Cover".

This conformance class is part of the [INSPIRE Data Specification on Land Cover](../README.md).

## Standardization target type

INSPIRE spatial data set

## Dependencies

### Direct dependencies

none

### Indirect dependencies

An indirect dependency is another conformance class whose requirements must be met by a related resource.

| Specification | Conformance class | Related resource | Parameters |
| ------------- | ----------------- | ---------------- | ---------- |
| [TG DS-LC](./README.md#ref_TG_DS_LC) | [GML application schemas, Land Cover](../lc-gml/README.md) | INSPIRE spatial data set encoded in GML, Land Cover features | n/a |
 
## Feature types <a name="feature-types"></a>

This application schema defines only a data type and a code list, used by feature types defined in the other two application schemas, Land Cover Raster and Land Cover Vector.


*Note*: When "features" or "spatial objects" are mentioned in the test cases, this refers to instances of feature types of the two application schemas, Land Cover Raster and Land Cover Vector.

## External document references

The following abbreviations are used in the test text for referring to external documents:

Abbreviation                     | Document name
-------------------------------- | --------------------------------------------------
TG DS-LC <a name="ref_TG_DS_LC"></a>   | [INSPIRE Data Specification on Land Cover – Technical Guidelines](https://knowledge-base.inspire.ec.europa.eu/publications/inspire-data-specification-land-cover-technical-guidelines_en)
TG DS Template <a name="ref_TG_DS_tmpl"></a>   | [INSPIRE Data Specification Template](https://knowledge-base.inspire.ec.europa.eu/publications/data-specifications-template_en)

## Test Cases

| Identifier                                                        | Status   | Test case in [TG DS-LC](#ref_TG_DS_LC)  |
| ----------------------------------------------------------------- | -------- | ------------ |
| [Constraints](./constraints.md)  | Draft  | A.1.6  |
| [Specific requirements](./specific-req.md)  | Draft  | A.1.6  |


## XML namespace prefixes <a name="namespaces"></a>

The following prefixes are used to refer to the corresponding XML namespaces in all test descriptions:

Prefix         | Namespace
-------------- | -------------------------------------------------
lcn    	 	   | http://inspire.ec.europa.eu/schemas/lcn/5.0
base           | http://inspire.ec.europa.eu/schemas/base/3.3
gml            | http://www.opengis.net/gml/3.2
wfs            | http://www.opengis.net/wfs/2.0
xsi            | http://www.w3.org/2001/XMLSchema-instance
xlink          | http://www.w3.org/1999/xlink
xml            | http://www.w3.org/XML/1998/namespace
