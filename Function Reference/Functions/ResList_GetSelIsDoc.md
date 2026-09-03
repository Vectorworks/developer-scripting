# ResList_GetSelIsDoc

## Description
Return if the selected resource is in the current document. The 'uniqueID' is a string identifier uniquely identifying this control.

```pascal
FUNCTION ResList_GetSelIsDoc(uniqueID : STRING): BOOLEAN;
```

```python
def vs.ResList_GetSelIsDoc(uniqueID):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|uniqueID|STRING|   |

## Examples
```pascal
{if (NOT useMaterialArchComp) THEN
	archCompMaterialNameID := '0'
ELSE BEGIN}
	localName := ResList_GetSel( kMaterialsContent1 );
	bSelInDoc := ResList_GetSelIsDoc(kMaterialsContent1);
	if (NOT bSelInDoc) THEN
		LocImageHandle	:= ResList_ImportItem( kMaterialsContent1 );
```
```python
import vs

# Return if the selected resource is in the current document.
uniqueID = 'Example'

ok = vs.ResList_GetSelIsDoc(uniqueID)
if ok:
    vs.Message('ResList_GetSelIsDoc succeeded')
else:
    vs.Message('ResList_GetSelIsDoc failed')
```

## Version
Availability: from Vectorworks 2017

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
