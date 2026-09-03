# PythonGetSearchPath

## Description
Return the search path for python files.

```pascal
FUNCTION PythonGetSearchPath : DYNARRAY[] of CHAR;
```

```python
def vs.PythonGetSearchPath():
    return DYNARRAY[] of CHAR
```

## Examples
```pascal
result := PythonGetSearchPath;
```
```python
import vs

# Return the search path for python files.
text = vs.PythonGetSearchPath()
vs.Message('PythonGetSearchPath returned: ' + str(text))
```

## See Also
VS Functions:
[PythonSetSearchPath](PythonSetSearchPath.md) 
| [PythonExecute](PythonExecute.md)

## Version
Availability: from Vectorworks 2014

## Category
* [Utility](../Categories/Utility.md)
