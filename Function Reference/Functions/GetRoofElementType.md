# GetRoofElementType

## Description
Returns information on the specified roof element.  The dormer type value is one of the following: 1 for Trapezium Dormer, 2 for Saddle Dormer, 3 for Shed Dormer, 4 for Slope Dormer, 5 for Bat Dormer.

```pascal
PROCEDURE GetRoofElementType(
				roofObject     : HANDLE;
				dormerID       : INTEGER;
				VAR edgeIndex  : INTEGER;
				VAR isDormer   : BOOLEAN;
				VAR dormerType : INTEGER);
```

```python
def vs.GetRoofElementType(roofObject, dormerID):
    return (edgeIndex, isDormer, dormerType)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|roofObject|HANDLE|Handle to roof object.|
|dormerID|INTEGER|Index of roof element.|
|edgeIndex|INTEGER|Index of roof edge associated with roof element (1-based index).|
|isDormer|BOOLEAN|True if this element is a dormer, false if it is a skylight.|
|dormerType|INTEGER|Type of dormer roof element.|

## Remarks
Get the type of roof object from id.

dormerID: Identifies the dormer for which to retrieve the information.
edgeIndex: Index to which roof face this skylight or dormer is placed.  Value is one based.

isDormer: true if this object is a dormer, false if skylight
dormerType: if it is a dormer then:

1 for Trapezium Dormer
2 for Saddle Dormer
3 for Shed Dormer
4 for Slope Dormer
5 for Bat Dormer

## Version
Availability: from VectorWorks9.0

## Category
* [Objects - Roofs](../Categories/Objects%20-%20Roofs.md)
