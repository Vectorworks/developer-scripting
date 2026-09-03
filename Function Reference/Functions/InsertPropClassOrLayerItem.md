# InsertPropClassOrLayerItem

## Description
Inserts a class or layer item in the proposed section of a Class, Design Layer, or Sheet Layer Layout Manager Pull Down.

Replaces [ InsertProposedClassOrLayerItem](InsertProposedClassOrLayerItem.md)

```pascal
FUNCTION InsertPropClassOrLayerItem(
				dialogID       : LONGINT;
				controlID      : LONGINT;
				strLabel       : STRING;
				imageSpecifier : DYNARRAY[] of CHAR): BOOLEAN;
```

```python
def vs.InsertPropClassOrLayerItem(dialogID, controlID, strLabel, imageSpecifier):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The dialog identifier given by the command to create the dialog.|
|controlID|LONGINT|The control identifier.|
|strLabel|STRING|Text for the label of the Pull Down.|
|imageSpecifier|DYNARRAY[] of CHAR|The string identifier for the image. It should be of the form &quot;ResourceFileNameWithoutExtension/PathOfImageFile&quot;.|

## Examples
```pascal
BEGIN
	{IF InsertProposedClassOrLayerItem(dialogID,  ItemID,  kContainerClass,  0) THEN}
	IF InsertPropClassOrLayerItem(dialogID,  ItemID,  kContainerClass,  '') THEN
		IF PartClass = '' THEN
			BEGIN
			IF Added then
				SelectChoice(dialogID,  ItemID, 2, TRUE)
			ELSE
				SelectChoice(dialogID,  ItemID, 1, TRUE);
			END

BEGIN
	{ boo := InsertProposedClassOrLayerItem(IDLabelDialog, kLabelClass,DefaultClass,0);}
	boo := InsertPropClassOrLayerItem(IDLabelDialog, kLabelClass,DefaultClass,'');
END;

	SetEditReal( dlgId, kSlabThicknessEdit, 3, pFloorThk );
	EnableItem(dlgId, kSlabThicknessEdit, TRUE );
END;
{AlrtDialog(concat( 'string3029 = ', GetPluginString( 3029 ) ) );}
boolD := InsertPropClassOrLayerItem( dlgId, kClassPopup, GetPluginString( 3029 ) ,'' );{ <Massing Model Class>}
SelectChoice( dlgId,  kClassPopup, 1, TRUE);
SetEditReal( dlgId, kElevationEdit, 3, dElevationInit );
SetEditReal( dlgId, kFloorHeightEdit, 3, dHeightInit );
SetItemText( dlgId, kEdit1, lString );
```
```python
import vs

# Inserts a class or layer item in the proposed section of a Class, Design
# Layer, or Sheet Layer Layout Manager Pull Down.
dialogID = 1
controlID = 2
strLabel = 'Example text'
imageSpecifier = 'Example'

ok = vs.InsertPropClassOrLayerItem(dialogID, controlID, strLabel, imageSpecifier)
if ok:
    vs.Message('InsertPropClassOrLayerItem succeeded')
else:
    vs.Message('InsertPropClassOrLayerItem failed')
```

## Version
Availability: from Vectorworks 2012

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
