# vsoGetPluginStyleSym

## Description
Allow an object to use its own implementation in creating and maintaining a plugin style

```pascal
PROCEDURE vsoGetPluginStyleSym(VAR hSymDef : HANDLE);
```

```python
def vs.vsoGetPluginStyleSym():
    return hSymDef
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hSymDef|HANDLE|   |

## Examples
```pascal
BEGIN
	{ Add New Parameters to Style if needed}
	vsoGetPluginStyleSym( styleHandle );
	bsb := AddToPluginStyle( styleHandle, 'Manufacturer', 0 );
	if ( bsb = TRUE ) THEN BEGIN
		bsb := AddToPluginStyle( styleHandle, 'Product Line', 0 );
		bsb := AddToPluginStyle( styleHandle, 'Overlay Door Style', 0 );

{ Add New Parameters to Style if needed}
vsoGetPluginStyleSym( styleHandle );
IF (styleHandle <> NIL ) THEN
BEGIN
	resultStatus :=  AddToPluginStyle( styleHandle, 'ArchCompMaterialID',	0 );
	resultStatus :=  AddToPluginStyle( styleHandle, 'StructCompMaterialID', 0 );

BEGIN
	vsoGetPluginStyleSym( styleHandle );
	result := AddToPIOStyleEdit( styleHandle, 'TextHeight', 2,  '' );
	result := AddToPIOStyleEdit( styleHandle, kArchHeightsAndOffsets, kRename, GetPlugInString( 3023 ) );
	vsoSetEventResult( kEditPluginStyleDefault );
END;
```
```python
import vs

# Allow an object to use its own implementation in creating and maintaining a
# plugin style.
result = vs.vsoGetPluginStyleSym()
```

## Version
Availability: from Vectorworks 2017

## Category
* [Object Events](../Categories/Object%20Events.md)
