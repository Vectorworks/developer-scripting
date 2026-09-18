# ResList_DlgInit

## Description
Use this call during dialog initialization to associate a popup control or resource popup and initialized by the ResList_* calls of the uniqueID identifying the resource list data.

```pascal
PROCEDURE ResList_DlgInit(
				uniqueID : STRING;
				dlgID    : INTEGER;
				ctrlID   : INTEGER);
```

```python
def vs.ResList_DlgInit(uniqueID, dlgID, ctrlID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|uniqueID|STRING|   |
|dlgID|INTEGER|   |
|ctrlID|INTEGER|   |

## Examples
```pascal
ResList_DlgInit( kMaterialsContent1, dialog1, kPopup23ArchMaterial );
ResList_RemRsrcCtrls(kMaterialsContent1);
ResList_AddRsrcCtrl(kMaterialsContent1, 0);

	ResList_Init( kSymbolsContent , kDefConResType );
	ResList_AddCont( kSymbolsContent, kDefConFoldID );
	ResList_DlgInit( kSymbolsContent, dialog, kImagePopup_ProfSyms );
END;

BEGIN
	{Resource Manager Hatch init}
	ResList_Init( kHatchContent, {kHatchDefNode}66 );
	ResList_AddCont( kHatchContent, kDefaultParkSpaceFolder );
	ResList_DlgInit( kHatchContent, dialogID, kHatchPopupID );
```
```python
import vs

# Use this call during dialog initialization to associate a popup control or
# resource popup and initialized by the ResList_* calls of the uniqueID
# identifying.
uniqueID = 'Example'
dlgID = 1
ctrlID = 2

vs.ResList_DlgInit(uniqueID, dlgID, ctrlID)
```

## Version
Availability: from Vectorworks 2017

## Category
* [Tool Events](../Categories/Tool%20Events.md)
