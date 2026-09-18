# Road_InsertStation

## Description
Insert a new station to the Roadway (Poly) object.

```pascal
PROCEDURE Road_InsertStation(
				hRoadwayObject : HANDLE;
				point          : REAL);
```

```python
def vs.Road_InsertStation(hRoadwayObject, point):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hRoadwayObject|HANDLE|   |
|point|REAL|   |

## Examples
```pascal
Road_InsertStation(hRoadwayObject, 1.0);
```
```python
import vs

# Insert a new station to the Roadway (Poly) object.
hRoadwayObject = vs.FSActLayer()  # handle to the first selected object on the active layer
point = 1.0

vs.Road_InsertStation(hRoadwayObject, point)
```

## Version
Availability: from Vectorworks 2015

## Category
* [Roadway Interface Library](../Categories/Roadway%20Interface%20Library.md)
