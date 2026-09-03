# GeogCoordToVW

## Description
Get point in Vectorworks coordinates.

```pascal
FUNCTION GeogCoordToVW(
				inLat         : REAL;
				inLon         : REAL;
				VAR outCoordX : REAL;
				VAR outCoordY : REAL): BOOLEAN;
```

```python
def vs.GeogCoordToVW(inLat, inLon):
    return (BOOLEAN, outCoord)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inLat|REAL|   |
|inLon|REAL|   |
|outCoordX|REAL|   |
|outCoordY|REAL|   |

## Examples
```pascal
isOK		:= VWCoordToGeog( locX, locY, lat, lon );
isOK		:= GeogCoordToVW( lat + 1, lon, northX, northY );
angleToN	:= Rad2Deg( ArcTan2(northY-LocY, northX-LocX) ) - 90;

textColumns := ParseString(dynaChar);
IF (ValidNumStr(textColumns[inColX], x)) & (ValidNumStr(textColumns[inColY], y)) & (ValidNumStr(textColumns[inColZ], z)) THEN BEGIN
	IF ( IsGeoreferenced( ActLayer ) AND gGeogrUnits ) THEN BEGIN
		isgeoref := GeogCoordToVW( x, y, x, y );
		z := ((z / importUPI) * _UPI);
	END
```
```python
import vs

# Get point in Vectorworks coordinates.
inLat = 1.0
inLon = 2.0

ok, outCoord = vs.GeogCoordToVW(inLat, inLon)
vs.Message('GeogCoordToVW returned: ' + str((ok, outCoord)))
```

## Version
Availability: from Vectorworks 2012

## Category
* [GIS](../Categories/GIS.md)
