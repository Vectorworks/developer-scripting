# TextLeading

## Description
Procedure TextLeading sets the default line spacing of VectorWorks to a custom leading value (in points).

```pascal
PROCEDURE TextLeading(leading : REAL);
```

```python
def vs.TextLeading(leading):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|leading|REAL|Custom leading value for document.|

## Examples
```pascal
TextLeading(1.0);
```
```python
import vs

# Procedure TextLeading sets the default line spacing of VectorWorks to a
# custom leading value (in points).
leading = 1.0

vs.TextLeading(leading)
```

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
