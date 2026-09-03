# GetObjectUuid

## Description
Function GetObjectUuid returns the UUID of the referenced object.

```pascal
FUNCTION GetObjectUuid(h : HANDLE): STRING;
```

```python
def vs.GetObjectUuid(h):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object|

## Examples
```pascal
		GetVWRString(temp_s, 'Raum CW/Strings/11612 *','1');
		spaces[space_cnt].name := temp_s;
	END;
	spaces[space_cnt].order := Str2Num(GetRField(h, 'Space', 'Matrix Order'));
	spaces[space_cnt].uid   := GetObjectUuid(h);
END;

BEGIN
	polyCnt := polyCnt + 1;
	polys[polyCnt].id := GetObjectUuid(h);
	polys[polyCnt].h := CopyPathPoly(h);
END;

h1 := GetObjectByUuid(space1);
if (h1 = nil) then BEGIN
	space1 := GetRField(objHand, objName, 'Space1');
	h1 := GetObject(space1);
	uuid := GetObjectUuid(h1);
	SetRField(objHand, objName, 'Space1UUID', uuid);
	{ AlrtDialog(CONCAT('Translating old Space Link to current, using uuid ', uuid)); }
END ELSE BEGIN
	{ the object name here may not be meaningful, but this is a best effort at backward compatibility }
```
```python
import vs

# Function GetObjectUuid returns the UUID of the referenced object.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

text = vs.GetObjectUuid(h)
vs.Message('GetObjectUuid returned: ' + str(text))
```

## See Also
VS Functions:
[GetObjectByUuid](GetObjectByUuid.md)

## Version
Availability: from Vectorworks 2018.4

## Category
* [Object Info](../Categories/Object%20Info.md)
