# InsertEnhanPullDownMenuItem

## Description
Inserts a image Replaces InsertEnhancedPulldownMenuItem

```pascal
FUNCTION InsertEnhanPullDownMenuItem(
				dialogID       : LONGINT;
				controlID      : LONGINT;
				strName        : STRING;
				imageSpecifier : DYNARRAY[] of CHAR): INTEGER;
```

```python
def vs.InsertEnhanPullDownMenuItem(dialogID, controlID, strName, imageSpecifier):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|   |
|controlID|LONGINT|   |
|strName|STRING|   |
|imageSpecifier|DYNARRAY[] of CHAR|The string identifier for the image. It should be of the form &quot;ResourceFileNameWithoutExtension/PathOfImageFile&quot;.|

## Version
Availability: from Vectorworks 2012

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
