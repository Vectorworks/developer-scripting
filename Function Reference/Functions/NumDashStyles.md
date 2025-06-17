# NumDashStyles

## Description
Function NumDashStyles returns the number of available line dash patterns.

```pascal
FUNCTION NumDashStyles : INTEGER;
```

```python
def vs.NumDashStyles():
    return INTEGER
```

## Remarks
*\_c\_*, 2014.04.08:  It returns exclusively the count of dash styles ignoring complex line types, if any. Use [BuildResourceList](BuildResourceList.md)  instead if you need them.

## Examples
#### VectorScript ####
```pascal
numLS := NumDashStyles;
```
#### Python ####
```python

```

## See Also
VS Functions:
[BuildResourceList](BuildResourceList.md) 
| [GetNameFromResourceList](GetNameFromResourceList.md)

## Version
Availability: from MiniCAD 4.0

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
