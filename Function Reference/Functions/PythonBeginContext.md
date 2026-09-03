# PythonBeginContext

## Description
This function creates a context in which PythonExecute scripts are run.<BR>
<BR>
This function consecutive python scripts to be executed inside the same python environment.

```pascal
PROCEDURE PythonBeginContext;
```

```python
def vs.PythonBeginContext():
    return None
```

## Examples
[PythonExecute](PythonExecute.md).

```pascal
PythonBeginContext;
```
```python
import vs

# This function creates a context in which PythonExecute scripts are run.
vs.PythonBeginContext()
```

## See Also
VS Functions:
[PythonExecute](PythonExecute.md) 
| [PythonEndContext](PythonEndContext.md)

## Version
Availability: from Vectorworks 2014

## Category
* [Utility](../Categories/Utility.md)
