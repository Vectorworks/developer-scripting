# vsoADPAddDimPlace

## Description
Add a dimension placement to a dimension type result that has begun for the Auto Dimension GetSupportedTypes (77) message sent to a Script object.

```pascal
PROCEDURE vsoADPAddDimPlace(
				message : LONGINT;
				dimType : INTEGER);
```

```python
def vs.vsoADPAddDimPlace(message, dimType):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|message|LONGINT|   |
|dimType|INTEGER|   |

## Examples
```pascal
vsoADPAddDimPlace(1, 2);
```
```python
import vs

# Add a dimension placement to a dimension type result that has begun for the
# Auto Dimension GetSupportedTypes (77) message sent to a Script object.
message = 'Hello Vectorworks'
dimType = 0

vs.vsoADPAddDimPlace(message, dimType)
```

## Version
Availability: from Vectorworks 2023

## Category
* [Object Events](../Categories/Object%20Events.md)
