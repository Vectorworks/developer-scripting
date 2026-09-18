# ResList_ImportItem

## Description
Import the currently selected item. This is the list that typically is created by call to BuildResourceList. The 'uniqueID' is a string identifier uniquely identifying this control.

```pascal
FUNCTION ResList_ImportItem(uniqueID : STRING): HANDLE;
```

```python
def vs.ResList_ImportItem(uniqueID):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|uniqueID|STRING|   |

## Examples
```pascal
ELSE BEGIN}
	localName := ResList_GetSel( kMaterialsContent1 );
	bSelInDoc := ResList_GetSelIsDoc(kMaterialsContent1);
	if (NOT bSelInDoc) THEN
		LocImageHandle	:= ResList_ImportItem( kMaterialsContent1 );

BEGIN
	symbolName := ResList_GetSel( kSymbolsContent );
	symHandle := ResList_ImportItem( kSymbolsContent );
	symbolWidth 	:= HWidth( symHandle );
	symbolHeight	:= HHeight( symHandle );
END;

BEGIN
	gVectorFillName := ResList_GetSel( kHatchContent );
	hatchIndex := ResList_ImportItem( kHatchContent );
	SetRField(gPluginH, GetName(recordHand), 'AisleColor', Num2Str(0, 0));
	SetRField(gPluginH, GetName(recordHand), 'AisleHatch', gVectorFillName);
	SetRField(gPluginH, GetName(recordHand), 'AislePattern', Num2Str(0, -1));
	SetRField(gPluginH, GetName(recordHand), 'AisleClass', '');
```
```python
import vs

# Import the currently selected item.
uniqueID = 'Example'

objHandle = vs.ResList_ImportItem(uniqueID)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2017

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
