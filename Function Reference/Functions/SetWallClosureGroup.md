# SetWallClosureGroup

## Description
Set wall closure geometry for a parametric object.<BR>
Currently only the first item in the group is used. All objects should be combined into a single solid.

```pascal
FUNCTION SetWallClosureGroup(
				objectHandle  : HANDLE;
				closureHandle : HANDLE): BOOLEAN;
```

```python
def vs.SetWallClosureGroup(objectHandle, closureHandle):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHandle|HANDLE|Handle to the plug-in object|
|closureHandle|HANDLE|Handle to the group containing the wall closure geometry.|

## Version
Availability: from Vectorworks 2022

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
