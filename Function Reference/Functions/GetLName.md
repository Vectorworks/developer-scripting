# GetLName

## Description
Function GetLName returns the name of the referenced layer.

```pascal
FUNCTION GetLName(h : HANDLE): STRING;
```

```python
def vs.GetLName(h):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to layer.|

## Remarks
Returns the name of the referenced layer.

[sd 8/14/98]

## Examples
[IsolateLayer](examples/IsolateLayer.md)

```pascal
actLayerH := actLayer;
IF GetLayer (h) <> NIL THEN Layer (GetLName (GetLayer (h)));
{Layer (GetLName (GetLayer (h)));}
getArcProps (objH, method, r, theta1, theta2, maxSegLength, x, y);

BEGIN
	gActlayName := GetLName(ActLayer);
	tmpQStr := Concat('((SEL) & (L = ',QStr(gActLayName),'))');
	ObjCount := 0;
	ObjCount := Count(tmpQStr);
	IF ObjCount > 0 THEN

{store the active Layer}
actLH := ActLayer;
{change the active Layer}
Layer( GetLName( GetLayer( textFoundH ) ) );
```
```python
activeLayerName = vs.GetLName( vs.ActLayer() )
```
See also in tutorials: [10. Iterate the Drawing and Report a Summary](ai%20examples/10_IterateAndReport.md), [22. Selected Objects → Worksheet Rows](ai%20examples/22_WorksheetSelectedObjects.md), [23. Count Objects by Criteria (Formula-Driven)](ai%20examples/23_WorksheetCountByCriteria.md), [25. Geometric Property Extraction Table](ai%20examples/25_WorksheetPolyGeometry.md)

## Version
Availability: from All Versions

## Category
* [Layers](../Categories/Layers.md)
