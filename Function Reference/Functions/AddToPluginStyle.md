# AddToPluginStyle

## Description
Adds a new item to a plug-in style map.

```pascal
FUNCTION AddToPluginStyle(
				hSymDef   : HANDLE;
				itemName  : STRING;
				styleType : INTEGER): BOOLEAN;
```

```python
def vs.AddToPluginStyle(hSymDef, itemName, styleType):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hSymDef|HANDLE|Handle to a symbol definition containing a plug-in style.|
|itemName|STRING|Name of new item to add.|
|styleType|INTEGER|Style type for new item. 0 sets the item to By Instance 1 sets the item to By style.|

## Version
Availability: from Vectorworks 2017

## Category
* [Objects - Symbols](../Categories/Objects%20-%20Symbols.md)
