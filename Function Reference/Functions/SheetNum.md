# SheetNum

## Description
Returns the number of saved views contained within the current document.

```pascal
FUNCTION SheetNum : INTEGER;
```

```python
def vs.SheetNum():
    return INTEGER
```

## Examples
```pascal
resultN := SheetNum;
```
```python
import vs

# Returns the number of saved views contained within the current document.
count = vs.SheetNum()
vs.Message('SheetNum returned: ' + str(count))
```

## See Also
VS Functions:
[SheetList](SheetList.md)

## Version
Availability: from VectorWorks10.0

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
