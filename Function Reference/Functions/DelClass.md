# DelClass

## Description
Deletes the specified class from the active document. If there are objects in the class to be deleted, they are reassigned to the None class.

```pascal
PROCEDURE DelClass(className : STRING);
```

```python
def vs.DelClass(className):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|className|STRING|Name of class to delete.|

## Examples
==== VectorScript ====
```pascal
DelClass('Future Construction');
```
==== Python ====
```python
vs.DelClass('Future Construction')
```

## Version
Availability: from All Versions

## Category
* [Classes](../Categories/Classes.md)
