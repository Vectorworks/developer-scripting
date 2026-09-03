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

## Examples
```pascal
resultOK := SetWallClosureGroup(objectHandle, closureHandle);
```
```python
import vs

# Set wall closure geometry for a parametric object.
objectHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
closureHandle = vs.NextSObj(vs.FSActLayer())  # handle to the next selected object

ok = vs.SetWallClosureGroup(objectHandle, closureHandle)
if ok:
    vs.Message('SetWallClosureGroup succeeded')
else:
    vs.Message('SetWallClosureGroup failed')
```

## Version
Availability: from Vectorworks 2022

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
