# FLSByClass

## Description
Function FLSByClass returns whether the global attributes are set to use the line style of the default class.

```pascal
FUNCTION FLSByClass : BOOLEAN;
```

```python
def vs.FLSByClass():
    return BOOLEAN
```

## Remarks
Returns whether the global attributes are set to use the line style of the default class.
[sd 8/19/98]

## Examples
#### VectorScript ####
```pascal
useClassLStyle:=FLSByClass;
```
#### Python ####
```python
useClassLStyle = vs.FLSByClass()
```

```pascal
resultOK := FLSByClass;
```
```python
import vs

# Function FLSByClass returns whether the global attributes are set to use
# the line style of the default class.
ok = vs.FLSByClass()
if ok:
    vs.Message('FLSByClass succeeded')
else:
    vs.Message('FLSByClass failed')
```

## Version
Availability: from VectorWorks8.0

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
