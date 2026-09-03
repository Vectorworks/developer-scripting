# CC_GetConnectorData

## Description
Returns the entry in the connector types table for a given connector. Column 1 = Description, 2 = Panel Connector symbol

```pascal
FUNCTION CC_GetConnectorData(
				connector : STRING;
				col_index : INTEGER) : STRING;
```

```python

def vs.CC_GetConnectorData(connector, col_index):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|connector|STRING||
|col_index|INTEGER||

## Examples
```pascal
resultStr := CC_GetConnectorData('Example', 1);
```
```python
import vs

# Returns the entry in the connector types table for a given connector.
connector = 'Example'
col_index = 1

text = vs.CC_GetConnectorData(connector, col_index)
vs.Message('CC_GetConnectorData returned: ' + str(text))
```

## Version
Availability: from Vectorworks 2025.2

## Category
* [ConnectCAD](../Categories/ConnectCAD.md)
