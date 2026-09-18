# ResList_AddRsrcCtrl

## Description
Adds a new resource control to the top bar of a resource popup. The 'uniqueID' is a string identifier uniquely identifying this control. 'controlID' is one of the values in the SResourceControl::DefaultID enumeration in IResourceManagerContent.h.

```pascal
PROCEDURE ResList_AddRsrcCtrl(
				uniqueID  : STRING;
				controlID : INTEGER);
```

```python

def vs.ResList_AddRsrcCtrl(uniqueID, controlID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|uniqueID|STRING||
|controlID|INTEGER||

## Examples
```pascal
ResList_DlgInit( kMaterialsContent1, dialog1, kPopup23ArchMaterial );
ResList_RemRsrcCtrls(kMaterialsContent1);
ResList_AddRsrcCtrl(kMaterialsContent1, 0);
```
```python
import vs

# Adds a new resource control to the top bar of a resource popup.
uniqueID = 'Example'
controlID = 1

vs.ResList_AddRsrcCtrl(uniqueID, controlID)
```

## Version
Availability: from Vectorworks 2024.4

## Category
* [Document List Handling](../Categories/Document List Handling.md)
