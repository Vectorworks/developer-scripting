# FindElement

## Description
Returns the element path of the specified element.

```pascal
FUNCTION FindElement(
				XMLHandle        : LONGINT;
				startElementPath : STRING;
				searchElement    : STRING;
				VAR foundPath    : STRING):INTEGER;
```

```python
def vs.FindElement(XMLHandle, startElementPath, searchElement):
    return (INTEGER, foundPath)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|XMLHandle|LONGINT|   |
|startElementPath|STRING|   |
|searchElement|STRING|   |
|foundPath|STRING|Output parameter.|

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [XML](../Categories/XML.md)
