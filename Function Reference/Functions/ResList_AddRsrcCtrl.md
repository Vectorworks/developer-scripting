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

## Version
Availability: from Vectorworks 2024.4

## Category
* [Document List Handling](../Categories/Document List Handling.md)

