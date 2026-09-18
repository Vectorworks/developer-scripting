# FFillColorByClass

## Description
Function FFillColorByClass returns whether the global attributes are set to use the fill colors of the default class.

```pascal
FUNCTION FFillColorByClass : BOOLEAN;
```

```python
def vs.FFillColorByClass():
    return BOOLEAN
```

## Remarks
Returns whether the global attributes are set to use the fill colors of the default class.
[sd 8/19/98]

## Examples
#### VectorScript ####
```pascal
useClassFillCol:=FFillColorByClass;
```
#### Python ####
```python
useClassFillCol = vs.FFillColorByClass()
```

```pascal
resultOK := FFillColorByClass;
```
```python
import vs

# Function FFillColorByClass returns whether the global attributes are set to
# use the fill colors of the default class.
ok = vs.FFillColorByClass()
if ok:
    vs.Message('FFillColorByClass succeeded')
else:
    vs.Message('FFillColorByClass failed')
```

## Version
Availability: from VectorWorks8.0

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
