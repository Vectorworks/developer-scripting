# IsPolyClosed

## Description
Returns true if the specified polyline or polygon is a closed shape, and false otherwise.

```pascal
FUNCTION IsPolyClosed(polyHandle : HANDLE): BOOLEAN;
```

```python
def vs.IsPolyClosed(polyHandle):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|polyHandle|HANDLE|   |

## Examples
```pascal
	END;
END
{BRACKET TYPE Group}
else if polygonh <> nil then BEGIN
	if Not IsPolyClosed( polygonH ) then BEGIN
		GetPolylineVertex( polygonH, 1, v1[1], v1[2], verttype, arcrad );
		GetPolylineVertex( polygonH, 4, v2[1], v2[2], verttype, arcrad );
		tempV := v1 - v2;
		tempV := UnitVec( tempV );
		tempV := tempV * Norm(v1 - v2)/2;

IF IsPolyClosed(GetCustomObjectPath(pluginH)) THEN
	gClosure := 1; {Set closure to None internally, but don't change the actual parameter}

IF IsPolyClosed( h ) THEN
BEGIN
	SetRField( gPluginObjH, 'IrrigationOutletDrip', 'Type', 'Drip Area' );
END ELSE
BEGIN
	SetRField( gPluginObjH, 'IrrigationOutletDrip', 'Type', 'Drip Line' );
END;
```
```python
import vs

# Returns true if the specified polyline or polygon is a closed shape, and
# false otherwise.
polyHandle = vs.FSActLayer()  # handle to the first selected object on the active layer

ok = vs.IsPolyClosed(polyHandle)
if ok:
    vs.Message('IsPolyClosed succeeded')
else:
    vs.Message('IsPolyClosed failed')
```
See also in tutorials: [25. Geometric Property Extraction Table](ai%20examples/25_WorksheetPolyGeometry.md)

## Version
Availability: from Vectorworks 2014

## Category
* [Objects - Polys](../Categories/Objects%20-%20Polys.md)
