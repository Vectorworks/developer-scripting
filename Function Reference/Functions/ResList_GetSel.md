# ResList_GetSel

## Description
Return the selected item from the popup. The 'uniqueID' is a string identifier uniquely identifying this control.

```pascal
FUNCTION ResList_GetSel(uniqueID : STRING): STRING;
```

```python
def vs.ResList_GetSel(uniqueID):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|uniqueID|STRING|   |

## Examples
```pascal
localName := '';
IF (archCompMaterialNameID = '') THEN
	localName := ResList_GetSel( kMaterialsContent1 )
ELSE BEGIN
	localName := archCompMaterialNameID;
END;

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
```
```python
import vs

# Return the selected item from the popup.
uniqueID = 'Example'

text = vs.ResList_GetSel(uniqueID)
vs.Message('ResList_GetSel returned: ' + str(text))
```

## Version
Availability: from Vectorworks 2017

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
