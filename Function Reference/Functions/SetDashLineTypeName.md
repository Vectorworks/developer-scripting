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

## Examples
```pascal
BEGIN
	CntrDashIndex := CheckLSN(-1);
	IF SetDashLineTypeName(CntrDashIndex,GetPlugInString(21001)) THEN BEGIN END;
	ResourceToFolder(kResFldStrngBlk,GetObject(GetPlugInString(21001)),kTypeLineDef,'');
END

BEGIN
	ToeDashIndex := CheckLSN(-1);
	IF SetDashLineTypeName(ToeDashIndex,GetPlugInString(12001)) THEN BEGIN END;
	ResourceToFolder(kResFldStrngBlk,GetObject(GetPlugInString(12001)),kTypeLineDef,'');
END

BEGIN
	RampBendDashIndex := CheckLSN(-1);
	IF SetDashLineTypeName(RampBendDashIndex,GetPlugInString(12001)) THEN BEGIN END;
	ResourceToFolder(kResFldStrngBlk,GetObject(GetPlugInString(12001)),kTypeLineDef,'');
END
```
```python
import vs

# Sets the dash style name for the specified dash style using its negated
# internal index.
DashStyleIndex = 1
DashStyleName = 'Example'

ok = vs.SetDashLineTypeName(DashStyleIndex, DashStyleName)
if ok:
    vs.Message('SetDashLineTypeName succeeded')
else:
    vs.Message('SetDashLineTypeName failed')
```

## See Also
VS Functions:
[GetDashLineTypeName](GetDashLineTypeName.md)

## Version
Availability: from Vectorworks 2019

## Category
* [Object Names](../Categories/Object%20Names.md)
