# CreateLayer

## Description
Creates a layer of the specified type.

layerType values:
Design = 1
Presentation	= 2

```pascal
FUNCTION CreateLayer(
				layerName : STRING;
				layerType : INTEGER): HANDLE;
```

```python
def vs.CreateLayer(layerName, layerType):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|layerName|STRING|   |
|layerType|INTEGER|   |

## Remarks
*\_c\_*, 2015.07.12: The layer type constants can be fetched using [GetObjectVariableInt](GetObjectVariableInt.md)(layerHandle, 154).

## Examples
```pascal
writeln('SheetNumber_UDS = ',gSheetInfo [sheetNum].SheetNumber_UDS, '   SheetNumber_Seq = ',gSheetInfo [sheetNum].SheetNumber_Seq);
}
				{ create the sheet layer using the correct sheet number }
				IF gUseVW_UDS THEN
					sheetLayerH := CreateLayer( gSheetInfo [sheetNum].SheetNumber_UDS, 2 )
				ELSE sheetLayerH := CreateLayer( gSheetInfo [sheetNum].SheetNumber_Seq, 2 );

{//// create an empty temp layer and make it visible in the viewport }
tempLayName := CreateUUID;
tempLayHand := CreateLayer( tempLayName, 1 );
boo := SetVPLayerVisibility( testVPHand, tempLayHand, 0 );

BEGIN
	getPrintArea (pageWidth, pageHeight);
	sheetLayerH := CreateLayer (Concat (GetPluginString (3020),'1'), 2);	{"Sheet Layer-1"}
	Layer (GetLName (sheetLayerH));
	SetDrawingRect (pageWidth, pageHeight);
END;
```
```python
import vs

# Creates a layer of the specified type.
layerName = 'Design Layer-1'
layerType = 0

layerHandle = vs.CreateLayer(layerName, layerType)
if layerHandle is not None:
    vs.Message('Created object handle: ' + str(layerHandle))
```
See also in tutorials: [07. Set Up Document Structure: Layers and Classes](ai%20examples/07_LayersAndClasses.md), [30. Publish Worksheet Image on a Sheet Layer](ai%20examples/30_WorksheetPublishOnSheet.md)

## Version
Availability: from VectorWorks 10.5

## Category
* [Layers](../Categories/Layers.md)
