# SetDefaultOpacity

## Description
Sets the default opacity to document.

```pascal
PROCEDURE SetDefaultOpacity(opacity : INTEGER);
```

```python
def vs.SetDefaultOpacity(opacity):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|opacity|INTEGER|The opacity as percent value in range [0-100].|

## Examples
```pascal
SetDefaultOpacity(1);
```
```python
import vs

# Sets the default opacity to document.
opacity = 1

vs.SetDefaultOpacity(opacity)
```

## Version
Availability: from VectorWorks13.0

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
