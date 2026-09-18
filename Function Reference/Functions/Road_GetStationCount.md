# Road_GetStationCount

## Description
Return count of stations of the Roadway (Poly) object.

```pascal
FUNCTION Road_GetStationCount(hRoadwayObject : HANDLE): LONGINT;
```

```python
def vs.Road_GetStationCount(hRoadwayObject):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hRoadwayObject|HANDLE|   |

## Examples
```pascal
resultN := Road_GetStationCount(hRoadwayObject);
```
```python
import vs

# Return count of stations of the Roadway (Poly) object.
hRoadwayObject = vs.FSActLayer()  # handle to the first selected object on the active layer

count = vs.Road_GetStationCount(hRoadwayObject)
vs.Message('Road_GetStationCount returned: ' + str(count))
```

## Version
Availability: from Vectorworks 2015

## Category
* [Roadway Interface Library](../Categories/Roadway%20Interface%20Library.md)
