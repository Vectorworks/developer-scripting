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

## Examples
```pascal
resultOK := IsCatalogParameter(hObj, 'Example');
```
```python
import vs

# Check if a parameter is defined in the catalog that has been associated
# with an object's plug-in style.
hObj = vs.FSActLayer()  # handle to the first selected object on the active layer
paramName = 'Example'

ok = vs.IsCatalogParameter(hObj, paramName)
if ok:
    vs.Message('IsCatalogParameter succeeded')
else:
    vs.Message('IsCatalogParameter failed')
```

## Version
Availability: from Vectorworks 2018

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
