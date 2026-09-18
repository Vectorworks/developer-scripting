# ResList_RemRsrcCtrls

## Description
Removes all resource controls previously added to the top bar of a resource popup. The 'uniqueID' is a string identifier uniquely identifying this control.

```pascal
PROCEDURE ResList_RemRsrcCtrls(uniqueID : STRING);
```

```python

def vs.ResList_RemRsrcCtrls(uniqueID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|uniqueID|STRING||

## Examples
```pascal
ResList_DlgInit( kMaterialsContent1, dialog1, kPopup23ArchMaterial );
ResList_RemRsrcCtrls(kMaterialsContent1);
ResList_AddRsrcCtrl(kMaterialsContent1, 0);
```
```python
import vs

# Removes all resource controls previously added to the top bar of a resource
# popup.
uniqueID = 'Example'

vs.ResList_RemRsrcCtrls(uniqueID)
```

## Version
Availability: from Vectorworks 2024.4

## Category
* [Document List Handling](../Categories/Document List Handling.md)
