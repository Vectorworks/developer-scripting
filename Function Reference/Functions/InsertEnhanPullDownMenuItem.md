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

## Examples
```pascal
resultN := InsertEnhanPullDownMenuItem(1, 2, 'Example', imageSpecifier);
```
```python
import vs

# Inserts a image Replaces InsertEnhancedPulldownMenuItem.
dialogID = 1
controlID = 2
strName = 'Example'
imageSpecifier = 'Example'

resultN = vs.InsertEnhanPullDownMenuItem(dialogID, controlID, strName, imageSpecifier)
vs.Message('InsertEnhanPullDownMenuItem returned: ' + str(resultN))
```

## Version
Availability: from Vectorworks 2012

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
