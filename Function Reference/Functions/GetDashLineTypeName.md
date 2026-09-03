# GetDashLineTypeName

## Description
Retrieves the dash style name for the specified dash style using its negated internal index.

```pascal
FUNCTION GetDashLineTypeName(DashStyleIndex : LONGINT): STRING;
```

```python
def vs.GetDashLineTypeName(DashStyleIndex):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|DashStyleIndex|LONGINT|The negated internal index of the dash style.|

## Remarks
This replaces GetDashStyleName

## Examples
```pascal
resultStr := GetDashLineTypeName(1);
```
```python
import vs

# Retrieves the dash style name for the specified dash style using its
# negated internal index.
DashStyleIndex = 1

name = vs.GetDashLineTypeName(DashStyleIndex)
vs.Message('GetDashLineTypeName returned: ' + str(name))
```

## See Also
VS Functions:
[SetDashLineTypeName](SetDashLineTypeName.md)

## Version
Availability: from Vectorworks 2019

## Category
* [Object Names](../Categories/Object%20Names.md)
