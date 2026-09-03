# ResList_SetSelCtrl

## Description
Sets the selected resource control of a resource popup. The 'uniqueID' is a string identifier uniquely identifying this control. 'controlID' is one of the values in the SResourceControl::DefaultID enumeration in IResourceManagerContent.h.

```pascal
PROCEDURE ResList_SetSelCtrl(
				uniqueID  : STRING;
				controlID : INTEGER);
```

```python

def vs.ResList_SetSelCtrl(uniqueID, controlID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|uniqueID|STRING||
|controlID|INTEGER||

## Examples
```pascal
{ResList_SetSel( kMaterialsContent1, localName );}
IF (archCompMaterialNameID = '') THEN
	ResList_SetSelCtrl(kMaterialsContent1, 0)
ELSE BEGIN
	ResList_SelFAvail( kMaterialsContent1, archCompMaterialNameID, FALSE, FALSE, FALSE)
END;
```
```python
import vs

# Sets the selected resource control of a resource popup.
uniqueID = 'Example'
controlID = 1

vs.ResList_SetSelCtrl(uniqueID, controlID)
```

## Version
Availability: from Vectorworks 2024.4

## Category
* [Document List Handling](../Categories/Document List Handling.md)
