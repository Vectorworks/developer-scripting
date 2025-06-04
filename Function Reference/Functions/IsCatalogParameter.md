# IsCatalogParameter

## Description
Check if a parameter is defined in the catalog that has been associated with an object's plug-in style.

```pascal
FUNCTION IsCatalogParameter(
				hObj      : HANDLE;
				paramName : STRING): BOOLEAN;
```

```python
def vs.IsCatalogParameter(hObj, paramName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObj|HANDLE|Handle to plug-in object|
|paramName|STRING|Name of parameter to check|

## Version
Availability: from Vectorworks 2018

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
