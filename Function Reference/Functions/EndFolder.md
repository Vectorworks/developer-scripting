# EndFolder

## Description
Procedure EndFolder completes symbol folder creation in VectorScript. When EndFolder is called, the any procedure calls defined since a call to BeginFolder are used to create symbols and/or symbol folders.

```pascal
PROCEDURE EndFolder;
```

```python
def vs.EndFolder():
    return None
```

## Examples
```pascal
EndFolder;
```
```python
import vs

# Procedure EndFolder completes symbol folder creation in VectorScript.
vs.EndFolder()
```

## Version
Availability: from All Versions

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
