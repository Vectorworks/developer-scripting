# CreateVP

## Description
Creates a viewport object. The specified parent handle may only be a layer or a group contained within a layer, nested or otherwise.

```pascal
FUNCTION CreateVP(parentHandle : HANDLE): HANDLE;
```

```python
def vs.CreateVP(parentHandle):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|parentHandle|HANDLE|   |

## Remarks
(*_c_*, 2015.02.25):  This invariably creates a VP with scale 1:1, view top-plan and all layers and classes set to invisible.

## Version
Availability: from VectorWorks 11.0

## Category
* [Objects - Groups](../Categories/Objects%20-%20Groups.md)
