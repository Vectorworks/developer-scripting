# GetPluginStyleSymbol

## Description
Retrieves the handled to a symbol that defines the plug-in style for a given plug-in object.<BR>
<BR>

```pascal
FUNCTION GetPluginStyleSymbol(
				hObject     : HANDLE;
				VAR hSymDef : HANDLE): BOOLEAN;
```

```python
def vs.GetPluginStyleSymbol(hObject, hSymDef):
    return (BOOLEAN, hSymDef)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|Handle to a plug-in object.|
|hSymDef|HANDLE|Hanlde to a symbol definition that contrains the plug-in style associated with hObject.|

## Examples
```pascal
resultOK := GetPluginStyleSymbol(hObject, hSymDef);
```
```python
import vs

# Retrieves the handled to a symbol that defines the plug-in style for a
# given plug-in object.
hObject = vs.FSActLayer()  # handle to the first selected object on the active layer
hSymDef = vs.GetObject('MySymbol')  # handle to a symbol definition

ok, hSymDef = vs.GetPluginStyleSymbol(hObject, hSymDef)
vs.Message('GetPluginStyleSymbol returned: ' + str((ok, hSymDef)))
```

## Version
Availability: from Vectorworks 2017

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
