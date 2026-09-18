# FFillPat

## Description
Function FFillPat returns the current fill pattern setting.

Fill patterns and their associated constants can be found in the [VectorScript Appendix](../Appendix/pages/Appendix%20E%20-%20Miscellaneous%20Selectors.md#fill-patterns).

```pascal
FUNCTION FFillPat : LONGINT;
```

```python
def vs.FFillPat():
    return LONGINT
```

## Examples
#### VectorScript ####
```pascal
currFillStyle:=FFillPat;
```
#### Python ####
```python
currFillStyle = vs.FFillPat()
```

```pascal
resultN := FFillPat;
```
```python
import vs

# Function FFillPat returns the current fill pattern setting.
resultN = vs.FFillPat()
vs.Message('FFillPat returned: ' + str(resultN))
```

## Version
Availability: from All Versions

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
