# DLDSetLoadDataReal

## Description
Using selector, sets default load data with real value for the parametric object.
Available selectors : kDLDSelectorWeight = 5.

```pascal
PROCEDURE DLDSetLoadDataReal(
				selector : INTEGER;
				value    : REAL);
```

```python
def vs.DLDSetLoadDataReal(selector, value):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|selector|INTEGER|   |
|value|REAL|   |

## Examples
```pascal
DLDSetLoadDataReal(1, 1.0);
```
```python
import vs

# Using selector, sets default load data with real value for the parametric
# object.
selector = 1
value = 1.0

vs.DLDSetLoadDataReal(selector, value)
```

## Version
Availability: from Vectorworks 2018

## Category
* [Truss Analysis](../Categories/Truss%20Analysis.md)
