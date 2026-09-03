# LDevice_GetAccCount

## Description
Get the count of accessories attached to a Lighting Device's cell.

```pascal
FUNCTION LDevice_GetAccCount(
				handle    : HANDLE;
				cellIndex : LONGINT): LONGINT;
```

```python
def vs.LDevice_GetAccCount(handle, cellIndex):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|handle|HANDLE|   |
|cellIndex|LONGINT|   |

## Examples
```pascal
BEGIN
	CheckInLegendSymbols(h, counter - 1 , -2);
	accCountCell := LDevice_GetAccCount(h, counter);
	For counterInner := 1 to accCountCell DO
	BEGIN
		CheckInLegendSymbols(h, counter - 1, counterInner - 1);
	END;

BEGIN
numAcc := LDevice_GetAccCount(H,i);
IF numAcc > 0 THEN
	BEGIN
	FOR k := 0 to numAcc-1 DO
		BEGIN
```
```python
import vs

# Get the count of accessories attached to a Lighting Device's cell.
handle = vs.FSActLayer()  # handle to the first selected object on the active layer
cellIndex = 1

count = vs.LDevice_GetAccCount(handle, cellIndex)
vs.Message('LDevice_GetAccCount returned: ' + str(count))
```

## Version
Availability: from Vectorworks 2021

## Category
* [Spotlight](../Categories/Spotlight.md)
