# SetDashLineTypeName

## Description
Sets the dash style name for the specified dash style using its negated internal index.

```pascal
FUNCTION SetDashLineTypeName(
				DashStyleIndex : LONGINT;
				DashStyleName  : STRING): BOOLEAN;
```

```python
def vs.SetDashLineTypeName(DashStyleIndex, DashStyleName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|DashStyleIndex|LONGINT|The negated internal index of the dash style to be named.|
|DashStyleName|STRING|The new name of the line type.|

## Remarks
This replaces SetDashStyleName.

## See Also
VS Functions:
[GetDashLineTypeName](GetDashLineTypeName.md)

## Version
Availability: from Vectorworks 2019

## Category
* [Object Names](../Categories/Object%20Names.md)
