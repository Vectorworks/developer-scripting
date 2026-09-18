# ResList_Init

## Description
Initialize a categories resource with resources of the specified type. The 'uniqueID' is a string identifier uniquely identifying this control.

```pascal
PROCEDURE ResList_Init(
				uniqueID   : STRING;
				objectType : INTEGER);
```

```python
def vs.ResList_Init(uniqueID, objectType):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|uniqueID|STRING|   |
|objectType|INTEGER|   |

## Examples
```pascal
{-------------- Arch material init -------------------- }
ResList_Init( kMaterialsContent1, kBuildingMaterialNodeID );
{ResList_ImportItem( kMaterialsContent1); }
ResList_AddCont( kMaterialsContent1, 0 );
{IF (archCompMaterialNameID = '') THEN
	ResList_AddCont( kMaterialsContent1, kDefaultMaterialsFolder )

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

# Initialize a categories resource with resources of the specified type.
uniqueID = 'Example'
objectType = 0

vs.ResList_Init(uniqueID, objectType)
```

## Version
Availability: from Vectorworks 2017

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
