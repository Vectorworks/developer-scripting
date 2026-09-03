# GetCableBreakData

## Description
Get cable break data. Data selectors - 'Name'. If the function is called on a cable break subpart the break index is ignored. If the function is called on a cable object you have to specify the break index.

```pascal
FUNCTION GetCableBreakData(
				hObj         : HANDLE;
				DataSelector : STRING;
				BreakIndex   : INTEGER) : STRING;
```

```python

def vs.GetCableBreakData(hObj, DataSelector, BreakIndex):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObj|HANDLE||
|DataSelector|STRING||
|BreakIndex|INTEGER||

## Examples
```pascal
resultStr := GetCableBreakData(hObj, 'Example', 1);
```
```python
import vs

# Get cable break data.
hObj = vs.FSActLayer()  # handle to the first selected object on the active layer
DataSelector = 'Example'
BreakIndex = 1

text = vs.GetCableBreakData(hObj, DataSelector, BreakIndex)
vs.Message('GetCableBreakData returned: ' + str(text))
```

## Version
Availability: from Vectorworks 2025.4

## Category
* [Objects - Cables](../Categories/Objects%20-%20Cables.md)
