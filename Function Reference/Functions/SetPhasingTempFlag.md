# SetPhasingTempFlag

## Description
Procedure SetPhasingTempFlag sets the passed in boolean as the temporary flag value for the passed in handle's phasing data.

```pascal
FUNCTION SetPhasingTempFlag(
				hObject   : HANDLE;
				tempValue : BOOLEAN) : BOOLEAN;
```

```python
def vs.SetPhasingTempFlag(hObject, tempValue):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|The handle to set the phasing temporary flag value of.|
|tempValue|BOOLEAN|The boolean temporary flag value to set for the passed in object's phasing data.|

## Returns
Returns a boolean to indicate a successful set of the phasing temp flag or a failure to set the phasing temp flag.

## See Also
VS Functions:
[GetPhasingTempFlag](GetPhasingTempFlag.md)

## Version
Availability: from Vectorworks 2027

## Category
* [Phasing](Categories/Phasing.md)

