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

## Version
Availability: from Vectorworks 2025.2

## Category
* [ConnectCAD](../Categories/ConnectCAD.md)

