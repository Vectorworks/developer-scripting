# ResList_SetSel

## Description
Set the selected item in the resource popup. The 'uniqueID' is a string identifier uniquely identifying this control.

```pascal
PROCEDURE ResList_SetSel(
				uniqueID : STRING;
				itemName : STRING);
```

```python
def vs.ResList_SetSel(uniqueID, itemName):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|uniqueID|STRING|   |
|itemName|STRING|   |

## Examples
```pascal
BEGIN
	ResList_Init( kRepetUnitSymbols, 16 );
	ResList_AddCont( kRepetUnitSymbols,  kDefConDetailObjects );
	ResList_SetSel( kRepetUnitSymbols, SymbolName);
	ResList_DlgInit( kRepetUnitSymbols, SelectRepSymbol, kImagePopup6 );
END;

ResList_Init( kLecternTex , 97 );
ResList_AddCont( kLecternTex, 157 );
ResList_DlgInit( kLecternTex, dialog, kTexturePop );
ResList_SetSel( kLecternTex, kNoTexture );

ResList_SetSel( ContentID, SelectedTexture );
```
```python
import vs

# Set the selected item in the resource popup.
uniqueID = 'Example'
itemName = 'Example'

vs.ResList_SetSel(uniqueID, itemName)
```

## Version
Availability: from Vectorworks 2017

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
