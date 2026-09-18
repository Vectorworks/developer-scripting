# FindAttribute

## Description
Returns the element path of the specified attribute.

```pascal
FUNCTION FindAttribute(
				XMLHandle          : LONGINT;
				startElementPath   : STRING;
				searchAttribute    : STRING;
				VAR foundPath      : STRING;
				VAR attributeValue : STRING):INTEGER;
```

```python
def vs.FindAttribute(XMLHandle, startElementPath, searchAttribute):
    return (INTEGER, foundPath, attributeValue)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|XMLHandle|LONGINT|   |
|startElementPath|STRING|   |
|searchAttribute|STRING|   |
|foundPath|STRING|Output parameter.|
|attributeValue|STRING|Output parameter.|

## Examples
```pascal
resultN := FindAttribute(1, 'file.txt', 'Example', 'file.txt', 'Example');
```
```python
import vs

# Returns the element path of the specified attribute.
XMLHandle = 1
startElementPath = 'C:/Temp'
searchAttribute = 'Example'

resultN, foundPath, attributeValue = vs.FindAttribute(XMLHandle, startElementPath, searchAttribute)
vs.Message('FindAttribute returned: ' + str((resultN, foundPath, attributeValue)))
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [XML](../Categories/XML.md)
