# GetCatalogItem

## Description
Show the plug-in item catalog dialog to choose an item defined in the catalog. The object will be updated with all parameters defiend in the catalog.

```pascal
FUNCTION GetCatalogItem(hObj : HANDLE): BOOLEAN;
```

```python
def vs.GetCatalogItem(hObj):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObj|HANDLE|Handle to plug-in object.|

## Examples
```pascal
resultOK := GetCatalogItem(hObj);
```
```python
import vs

# Show the plug-in item catalog dialog to choose an item defined in the catalog.
hObj = vs.FSActLayer()  # handle to the first selected object on the active layer

ok = vs.GetCatalogItem(hObj)
if ok:
    vs.Message('GetCatalogItem succeeded')
else:
    vs.Message('GetCatalogItem failed')
```

## Version
Availability: from Vectorworks 2018

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
