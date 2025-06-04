# IsLocked

## Description
Returns is the object locked for edit.

```pascal
FUNCTION IsLocked(VAR hObject : HANDLE): BOOLEAN;
```

```python
def vs.IsLocked(hObject):
    return (BOOLEAN, hObject)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|Handle to the object|

## Examples
```python
isLocked := vs.IsLocked( object );
```

## Version
Availability: from Vectorworks 2025

## Category
* [Object Info](../Categories/Object%20Info.md)
