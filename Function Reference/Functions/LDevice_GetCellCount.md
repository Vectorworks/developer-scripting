# LDevice_GetCellCount

## Description
Get the count of cells attached to a Lighting Device.

```pascal
FUNCTION LDevice_GetCellCount(handle : HANDLE): LONGINT;
```

```python
def vs.LDevice_GetCellCount(handle):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|handle|HANDLE|   |

## Examples
```pascal
BEGIN
	needsLabelReset 	:= FALSE;
	cellCountLDevice 	:= LDevice_GetCellCount(h);
	For counter := 1 to cellCountLDevice DO
	BEGIN
		CheckInLegendSymbols(h, counter - 1 , -2);
		accCountCell := LDevice_GetAccCount(h, counter);

BEGIN
numCell := LDevice_GetCellCount(H);
FOR i := 0 to numCell-1 DO
	BEGIN
	numAcc := LDevice_GetAccCount(H,i);
	IF numAcc > 0 THEN
```
```python
import vs

# Get the count of cells attached to a Lighting Device.
handle = vs.FSActLayer()  # handle to the first selected object on the active layer

count = vs.LDevice_GetCellCount(handle)
vs.Message('LDevice_GetCellCount returned: ' + str(count))
```

## Version
Availability: from Vectorworks 2021

## Category
* [Spotlight](../Categories/Spotlight.md)
