# DT_AssociateWithObj

## Description
Returns TRUE if associating is successful.

```pascal
FUNCTION DT_AssociateWithObj(
				hDataTag : HANDLE;
				hObject  : HANDLE): BOOLEAN;
```

```python
def vs.DT_AssociateWithObj(hDataTag, hObject):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hDataTag|HANDLE|   |
|hObject|HANDLE|   |

## Examples
```pascal
dx := Str2Num( GetRField( stakeHandle, 'Stake Object', 'ControlPoint01X' ) );
dy := Str2Num( GetRField( stakeHandle, 'Stake Object', 'ControlPoint01Y' ) );
tagHandle := CreateCustomObjectN( 'Data Tag',x + dx, y + dy, rotation, FALSE );
valid := SetPluginStyle( tagHandle, strTagStyle );
valid := DT_AssociateWithObj( tagHandle, stakeHandle );
END;
```
```python
import vs

# Returns TRUE if associating is successful.
hDataTag = vs.FSActLayer()  # handle to the first selected object on the active layer
hObject = vs.NextSObj(vs.FSActLayer())  # handle to the next selected object

ok = vs.DT_AssociateWithObj(hDataTag, hObject)
if ok:
    vs.Message('DT_AssociateWithObj succeeded')
else:
    vs.Message('DT_AssociateWithObj failed')
```

## Version
Availability: from Vectorworks 2020

## Category
* [Data Tag Interface Library](../Categories/Data%20Tag%20Interface%20Library.md)
