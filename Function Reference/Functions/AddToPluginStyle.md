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

## Examples
```pascal
BEGIN
	{ Add New Parameters to Style if needed}
	vsoGetPluginStyleSym( styleHandle );
	bsb := AddToPluginStyle( styleHandle, 'Manufacturer', 0 );
	if ( bsb = TRUE ) THEN BEGIN
		bsb := AddToPluginStyle( styleHandle, 'Product Line', 0 );
		bsb := AddToPluginStyle( styleHandle, 'Overlay Door Style', 0 );
		bsb := AddToPluginStyle( styleHandle, 'Cabinet Type', 0 );

BEGIN
	resultStatus :=  AddToPluginStyle( styleHandle, 'ArchCompMaterialID',	0 );
	resultStatus :=  AddToPluginStyle( styleHandle, 'StructCompMaterialID', 0 );
	resultStatus :=  AddToPluginStyle( styleHandle, 'TexturesByMaterial',	0 );
END;
```
```python
import vs

# Adds a new item to a plug-in style map.
hSymDef = vs.GetObject('MySymbol')  # handle to a symbol definition
itemName = 'Example'
styleType = 0

ok = vs.AddToPluginStyle(hSymDef, itemName, styleType)
if ok:
    vs.Message('AddToPluginStyle succeeded')
else:
    vs.Message('AddToPluginStyle failed')
```

## Version
Availability: from Vectorworks 2017

## Category
* [Objects - Symbols](../Categories/Objects%20-%20Symbols.md)
