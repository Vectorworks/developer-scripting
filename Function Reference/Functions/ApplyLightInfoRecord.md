# ApplyLightInfoRecord

## Description
Apply Light Info Record from a symbol to an object.

```pascal
PROCEDURE ApplyLightInfoRecord(
				hSymboL : HANDLE;
				hObject : HANDLE);
```

```python
def vs.ApplyLightInfoRecord(hSymboL, hObject):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hSymboL|HANDLE|   |
|hObject|HANDLE|   |

## Examples
```pascal
ApplyLightInfoRecord(GetObject(SymName), ObjHandle); {Apply from record defaults}
ApplyLightInfoRecord(SymHandle, ObjHandle); {Apply from the object in the document}

BEGIN
	ResetObject(h);
	symName:=GetRField(h, kIObName, kIObSymbol);
	ApplyLightInfoRecord( GetObject( symName ), h );
END;
```
```python
import vs

# Apply Light Info Record from a symbol to an object.
hSymboL = vs.FSActLayer()  # handle to the first selected object on the active layer
hObject = vs.NextSObj(vs.FSActLayer())  # handle to the next selected object

vs.ApplyLightInfoRecord(hSymboL, hObject)
```

## Version
Availability: from Vectorworks 2013

## Category
* [Spotlight](../Categories/Spotlight.md)
