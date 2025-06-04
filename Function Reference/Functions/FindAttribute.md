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

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [XML](../Categories/XML.md)
