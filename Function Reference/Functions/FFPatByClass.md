# FFPatByClass

## Description
Function FFPatByClass returns whether the global attributes are set to use the fill pattern of the default class.

```pascal
FUNCTION FFPatByClass : BOOLEAN;
```

```python
def vs.FFPatByClass():
    return BOOLEAN
```

## Remarks
Returns whether the global attributes are set to use the fill pattern of the default class.

[sd 8/19/98]

## Examples
#### VectorScript ####
```pascal
useClassFPat:=FFPatByClass;
```
#### Python ####
```python
useClassFPat = vs.FFPatByClass()
```

```pascal
resultOK := FFPatByClass;
```
```python
import vs

# Function FFPatByClass returns whether the global attributes are set to use
# the fill pattern of the default class.
ok = vs.FFPatByClass()
if ok:
    vs.Message('FFPatByClass succeeded')
else:
    vs.Message('FFPatByClass failed')
```

## Version
Availability: from VectorWorks8.0

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
