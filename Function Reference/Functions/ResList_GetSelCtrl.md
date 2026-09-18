# ResList_GetSelCtrl

## Description
Gets the selected resource control of a resource popup. The 'uniqueID' is a string identifier uniquely identifying this control. The return value is one of the values in the SResourceControl::DefaultID enumeration in IResourceManagerContent.h.

```pascal
FUNCTION ResList_GetSelCtrl(uniqueID : STRING) : INTEGER;
```

```python

def vs.ResList_GetSelCtrl(uniqueID):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|uniqueID|STRING||

## Examples
```pascal
resultN := ResList_GetSelCtrl('Example');
```
```python
import vs

# Gets the selected resource control of a resource popup.
uniqueID = 'Example'

resultN = vs.ResList_GetSelCtrl(uniqueID)
vs.Message('ResList_GetSelCtrl returned: ' + str(resultN))
```

## Version
Availability: from Vectorworks 2024.4

## Category
* [Document List Handling](../Categories/Document List Handling.md)
