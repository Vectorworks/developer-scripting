# UndoOff

## Description
Procedure UndoOff clears the undo table and suspends undo for the remainder of the VectorScript procedure. The undo system resumes after the procedure is completed.

```pascal
PROCEDURE UndoOff;
```

```python
def vs.UndoOff():
    return None
```

## Examples
```pascal
UndoOff;
```
```python
import vs

# Procedure UndoOff clears the undo table and suspends undo for the remainder
# of the VectorScript procedure.
vs.UndoOff()
```

## Version
Availability: from VectorWorks8.0

## Category
* [Utility](../Categories/Utility.md)
