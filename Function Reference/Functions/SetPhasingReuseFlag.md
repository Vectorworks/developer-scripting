# SetPhasingReuseFlag

## Description
Procedure SetPhasingReuseFlag sets the passed in boolean as the reuse flag value for the passed in handle's phasing data.

```pascal
FUNCTION SetPhasingReuseFlag(
				hObject    : HANDLE;
				reuseValue : BOOLEAN) : BOOLEAN;
```

```python
def vs.SetPhasingReuseFlag(hObject, reuseValue):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|The handle to set the phasing reuse flag value of.|
|reuseValue|BOOLEAN|The boolean reuse flag value to set for the passed in object's phasing data.|

## Returns
Returns a boolean to indicate a successful set of the phasing reuse flag or a failure to set the phasing reuse flag.

## See Also
VS Functions:
[GetPhasingReuseFlag](GetPhasingReuseFlag.md)

## Version
Availability: from Vectorworks 2027

## Category
* [Phasing](Categories/Phasing.md)

