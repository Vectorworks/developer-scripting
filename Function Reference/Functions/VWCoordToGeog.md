# VWCoordToGeog

## Description
Get geographical coordinates of a point (latitude and longitude).

```pascal
FUNCTION VWCoordToGeog(
				inCoordX   : REAL;
				inCoordY   : REAL;
				VAR outLat : REAL;
				VAR outLon : REAL): BOOLEAN;
```

```python
def vs.VWCoordToGeog(inCoordX, inCoordY):
    return (BOOLEAN, outLat, outLon)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inCoordX|REAL|   |
|inCoordY|REAL|   |
|outLat|REAL|   |
|outLon|REAL|   |

## Examples
```pascal
end;
if NOT notFound then begin
	{get site model's position}
	HCenter( obj, locX, locY );
	isOK	:= VWCoordToGeog( locX, locY, lat, lon );
	if isOK then begin
		gLatitudeStr	:= Num2StrF( lat );
		gLongitudeStr	:= Num2StrF( lon );
	end

isOK		:= VWCoordToGeog( locX, locY, lat, lon );
isOK		:= GeogCoordToVW( lat + 1, lon, northX, northY );
angleToN	:= Rad2Deg( ArcTan2(northY-LocY, northX-LocX) ) - 90;
```
```python
import vs

# Get geographical coordinates of a point (latitude and longitude).
inCoordX = 1.0
inCoordY = 2.0

ok, outLat, outLon = vs.VWCoordToGeog(inCoordX, inCoordY)
vs.Message('VWCoordToGeog returned: ' + str((ok, outLat, outLon)))
```

## Version
Availability: from Vectorworks 2012

## Category
* [GIS](../Categories/GIS.md)
