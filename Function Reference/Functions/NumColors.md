# NumColors

## Description
Returns the last used color index in the current document.

```pascal
FUNCTION NumColors : INTEGER;
```

```python
def vs.NumColors():
    return INTEGER
```

## Examples
```pascal
resultN := NumColors;
```
```python
import vs

# Returns the last used color index in the current document.
count = vs.NumColors()
vs.Message('NumColors returned: ' + str(count))
```

## Version
Availability: from VectorWorks13.0

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
