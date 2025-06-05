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

## Version
Availability: from Vectorworks 2012

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
