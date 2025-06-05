# TextSpace

## Description
Procedure TextSpace sets the active spacing for a VectorWorks document. 

**Table - Text Spacing**

| Leading        | Constant |
|----------------|----------|
| Single space   | 2        |
| 1 1/2 space    | 3        |
| Double space   | 4        |

```pascal
PROCEDURE TextSpace(spacing : INTEGER);
```

```python
def vs.TextSpace(spacing):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|spacing|INTEGER|Spacing style for text.|

## Examples
#### VectorScript ####
```pascal
TextSpace(4);
{set the active leading to double space}
```
#### Python ####
```python

```

## Version
Availability: from All Versions

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
