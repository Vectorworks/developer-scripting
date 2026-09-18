# ResList_AddCont

## Description
Adds a content location. The 'uniqueID' is a string identifier uniquely identifying this control.

```pascal
PROCEDURE ResList_AddCont(
				uniqueID   : STRING;
				folderSpec : INTEGER);
```

```python
def vs.ResList_AddCont(uniqueID, folderSpec):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|uniqueID|STRING|   |
|folderSpec|INTEGER|   |

## Examples
```pascal
{-------------- Arch material init -------------------- }
ResList_Init( kMaterialsContent1, kBuildingMaterialNodeID );
{ResList_ImportItem( kMaterialsContent1); }
ResList_AddCont( kMaterialsContent1, 0 );
{IF (archCompMaterialNameID = '') THEN
	ResList_AddCont( kMaterialsContent1, kDefaultMaterialsFolder )
ELSE
	ResList_AddCont( kMaterialsContent1, 0 ); }

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

# Adds a content location.
uniqueID = 'Example'
folderSpec = 1

vs.ResList_AddCont(uniqueID, folderSpec)
```

## Version
Availability: from Vectorworks 2017

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
