# SetDashStyleName

## Description
Sets the dash style name of the specified dash style index.

```pascal
FUNCTION SetDashStyleName(
				DashStyleIndex : INTEGER;
				DashStyleName  : STRING): BOOLEAN;
```

```python
def vs.SetDashStyleName(DashStyleIndex, DashStyleName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|DashStyleIndex|INTEGER|The index of the dash style to be named.|
|DashStyleName|STRING|The new name of the dash style specified by the index.|

## Remarks
[[User:CBM-c-|_c_]], (2014.04.08):  This sets the name in the dash style list, not in the name list. It seems to be a left over from the time before introduction of dash styles as named resources.

## See Also
VS Functions:
[GetDashStyleName](GetDashStyleName.md)

## Version
Availability: from Vectorworks 2011

## Category
* [Object Names](../Categories/Object%20Names.md)
