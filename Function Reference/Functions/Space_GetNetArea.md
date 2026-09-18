# Space_GetNetArea

## Description
Returns net area of given space object

```pascal
FUNCTION Space_GetNetArea(space : HANDLE): REAL;
```

```python
def vs.Space_GetNetArea(space):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|space|HANDLE|   |

## Examples
```pascal
	GetVWRString(temp_s, 'Raum CW/Strings/11612 *','1');
	spaces[space_cnt].name := temp_s;
END;
spaces[space_cnt].dept  := GetRField(h, 'Space', 'Occupancy Type');
spaces[space_cnt].area  := Space_GetNetArea(h);
{AlrtDialog(Concat('LoadSpaceArray ', spaces[space_cnt].name, ' area: ', spaces[space_cnt].area));}
spaces[space_cnt].layer := GetLName(GetLayer(h));
IF IsFPatByClass(h)
	THEN spaces[space_cnt].FP := GetClFPat(GetClass(h))
```
```python
import vs

# Returns net area of given space object.
space = vs.FSActLayer()  # handle to the first selected object on the active layer

area = vs.Space_GetNetArea(space)
vs.Message('Space_GetNetArea returned: ' + str(area))
```

## Version
Availability: from Vectorworks 2014

## Category
* [SpaceObjectCoreTools](../Categories/SpaceObjectCoreTools.md)
