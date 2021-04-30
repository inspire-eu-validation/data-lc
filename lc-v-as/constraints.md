# Constraints

**Purpose**: Verify that the features provided in the dataset adhere to the constraints specified in the INSPIRE application schema.

**Prerequisites**

**Test method**

The following checks are performed for every feature in the dataset.

* **geometryIsKindOfGM_PointOrGM_Surface**: Check that [geometries](#geometries) of the LandCoverUnit feature types are points or surfaces (OCL: inv:self.geometry->forAll(l | l.oclIsKindOf(GM_Surface) or l.oclIsKindOf(GM_Point))).

* **coveredPercentagesLowerThan100**: Check that the sum of all [coveredPercentage](#coveredPercentage) attributes attached to each LandCoverObservation are lower or equal to 100 (OCL: inv:mosaic.coveredPercentage.sum() <= 100).


**Reference(s)**: 

* [TG DS Template](./README.md#ref_TG_DS_tmpl) IR requirement Article 4 (2)
* [TG DS-LC](./README.md#ref_TG_DS_LC) 5.5.2.1.2., 5.5.2.2.1.

**Test type**: Automated

**Notes** 

GM_Surface is implemented in GML by: gml:Surface, gml:Polygon, gml:PolyhedralSurface and gml:TriangulatedSurface.
GM_Point is implemented in GML by gml:Point.  

Verify that the OCL constraints that are specified in the UML model of the application schema are met, i.e. validate features against the constraints. For unmet constraints report [constraintViolation](#constraintViolation).

## Messages

Identifier  |  Message text (parameters start with '$')
---------------------------------------------------------- | -------------------------------------------------------------------------
constraintViolation <a name="constraintViolation"/>  |  XML document '$filename', $featureType '$gmlid': The constraint '$constraint' is violated.

## Contextual XPath references

The namespace prefixes used as described in [README](./README.md#namespaces).

Abbreviation                                               |  XPath expression                     |Multiplicity       |Voidable
---------------------------------------------------------- | ------------------------------------- | ------------------|----------
LandCoverUnit geometry <a name="geometries"></a> | //schema-element(lcv:LandCoverUnit)/lcv:geometry/gml:Surface <br> //schema-element(lcv:LandCoverUnit)/lcv:geometry/gml:Polygon <br> //schema-element(lcv:LandCoverUnit)/lcv:geometry/gml:PolyhedralSurface <br> //schema-element(lcv:LandCoverUnit)/lcv:geometry/gml:TriangulatedSurface <br> //schema-element(lcv:LandCoverUnit)/lcv:geometry/gml:Point <br> //schema-element(lcv:LandCoverDataset)/lcv:member/lcv:LandCoverUnit/lcv:geometry/gml:Surface <br> //schema-element(lcv:LandCoverDataset)/lcv:member/lcv:LandCoverUnit/lcv:geometry/gml:Polygon <br> //schema-element(lcv:LandCoverDataset)/lcv:member/lcv:LandCoverUnit/lcv:geometry/gml:PolyhedralSurface <br> //schema-element(lcv:LandCoverDataset)/lcv:member/lcv:LandCoverUnit/lcv:geometry/gml:TriangulatedSurface <br> //schema-element(lcv:LandCoverDataset)/lcv:member/lcv:LandCoverUnit/lcv:geometry/gml:Point | 1 | No
coveredPercentage <a name="coveredPercentage"></a> | //schema-element(lcv:LandCoverUnit)/lcv:landCoverObservation/lcv:LandCoverObservation/lcv:mosaic/lcv:LandCoverValue/lcv:coveredPercentage <br> //schema-element(lcv:LandCoverDataset)/lcv:member/lcv:LandCoverUnit/lcv:landCoverObservation/lcv:LandCoverObservation/lcv:mosaic/lcv:LandCoverValue/lcv:coveredPercentage | 1 | Yes
