# CC_GetSignalData

## Description
Returns the entry in the signal types table for a given signal. Column 1 = Prefix, 2 = Connector, 3 = Description

```pascal
FUNCTION CC_GetSignalData(
				signal    : STRING;
				col_index : INTEGER) : STRING;
```

```python

def vs.CC_GetSignalData(signal, col_index):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|signal|STRING||
|col_index|INTEGER||

## Examples
```pascal
resultStr := CC_GetSignalData('Example', 1);
```
```python
import vs

# Returns the entry in the signal types table for a given signal.
signal = 'Example'
col_index = 1

text = vs.CC_GetSignalData(signal, col_index)
vs.Message('CC_GetSignalData returned: ' + str(text))
```

## Version
Availability: from Vectorworks 2025.2

## Category
* [ConnectCAD](../Categories/ConnectCAD.md)
