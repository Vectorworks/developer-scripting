# GetWSRowHLockState

## Description
Returns the lock state of a row in the referenced worksheet

Note: If a row height is locked, the row will not automatically resize to fit the contents of the cells when text is entered.

```pascal
PROCEDURE GetWSRowHLockState(
				worksheet     : HANDLE;
				row           : INTEGER;
				VAR lockState : BOOLEAN);
```

```python
def vs.GetWSRowHLockState(worksheet, row):
    return lockState
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet|
|row|INTEGER|Worksheet row index|
|lockState|BOOLEAN|Row Height lock state ( returns TRUE is row height is locked ; FALSE otherwise)|

## Examples
#### VectorScript ####
```pascal
{Gets the lock state of the fifth row in the specified worksheet}
GetWSRowHLockState(sheet,5,lockstate);
```
#### Python ####
```python
lockstate = vs.GetWSRowHLockState(sheet,5)
```

```pascal
GetWSRowHLockState(worksheet, 1, TRUE);
```
```python
import vs

# Returns the lock state of a row in the referenced worksheet Note: If a row
# height is locked, the row will not automatically resize to fit the contents
# of the.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
row = 10

result = vs.GetWSRowHLockState(worksheet, row)
```

## Version
Availability: from VectorWorks12.0

## Category
* [Worksheets](../Categories/Worksheets.md)
