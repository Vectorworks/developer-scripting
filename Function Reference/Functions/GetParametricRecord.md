# GetParametricRecord

## Description
Returns the handle to the parametric record attached the referenced object.<BR>
<BR>
Parametric record is a hidden record format containing the parameter values of the parametric object.<BR>
Only parametric objects have parametric records.

```pascal
FUNCTION GetParametricRecord(h : HANDLE): HANDLE;
```

```python
def vs.GetParametricRecord(h):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to a parametric object|

## Version
Availability: from Vectorworks 2011

## Category
* [Database @ Record](../Categories/Database%20-%20Record.md)
