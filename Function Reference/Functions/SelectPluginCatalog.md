# SelectPluginCatalog

## Description
Brings up a dialog to select a catalog to attach to a plug-in style, change the attached catalog, or detach the current catalog.

```pascal
FUNCTION SelectPluginCatalog(hSymbol : HANDLE): BOOLEAN;
```

```python
def vs.SelectPluginCatalog(hSymbol):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hSymbol|HANDLE|Handle to a symbol the defines a plug-in style.|

## Examples
```pascal
resultOK := SelectPluginCatalog(hSymbol);
```
```python
import vs

# Brings up a dialog to select a catalog to attach to a plug-in style, change
# the attached catalog, or detach the current catalog.
hSymbol = vs.FSActLayer()  # handle to the first selected object on the active layer

ok = vs.SelectPluginCatalog(hSymbol)
if ok:
    vs.Message('SelectPluginCatalog succeeded')
else:
    vs.Message('SelectPluginCatalog failed')
```

## Version
Availability: from Vectorworks 2018

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
