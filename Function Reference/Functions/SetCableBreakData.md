# SetCableBreakData

## Description
Set cable break data. Data selectors - 'Name'. If the function is called on a cable break subpart the break index is ignored. If the function is called on a cable object you have to specify the break index.

```pascal
PROCEDURE SetCableBreakData(
				hObj         : HANDLE;
				DataSelector : STRING;
				BreakIndex   : INTEGER;
				Value        : STRING);
```

```python

def vs.SetCableBreakData(hObj, DataSelector, BreakIndex, Value):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObj|HANDLE||
|DataSelector|STRING||
|BreakIndex|INTEGER||
|Value|STRING||

## Examples
```pascal
SetCableBreakData(hObj, 'Example', 1, 'Example');
```
```python
import vs

# Set cable break data.
hObj = vs.FSActLayer()  # handle to the first selected object on the active layer
DataSelector = 'Example'
BreakIndex = 1
Value = 'Example'

vs.SetCableBreakData(hObj, DataSelector, BreakIndex, Value)
```

## Version
Availability: from Vectorworks 2025.4

## Category
* [Objects - Cables](../Categories/Objects%20-%20Cables.md)
