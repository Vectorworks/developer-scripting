# vsoADPGetDimDefParms

## Description
Retrieve the parameters from the Auto Dimension GetDimensionDefinitions (78) message sent to a Script object.

```pascal
PROCEDURE vsoADPGetDimDefParms(
				message           : LONGINT;
				VAR viewType      : INTEGER;
				VAR universalName : DYNARRAY[] of CHAR;
				VAR dimType       : INTEGER);
```

```python
def vs.vsoADPGetDimDefParms(message):
    return (viewType, universalName, dimType)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|message|LONGINT|   |
|viewType|INTEGER|   |
|universalName|DYNARRAY[] of CHAR|   |
|dimType|INTEGER|   |

## Examples
```pascal
vsoADPGetDimDefParms(1, 2, universalName, 3);
```
```python
import vs

# Retrieve the parameters from the Auto Dimension GetDimensionDefinitions
# (78) message sent to a Script object.
message = 'Hello Vectorworks'

viewType, universalName, dimType = vs.vsoADPGetDimDefParms(message)
vs.Message('vsoADPGetDimDefParms returned: ' + str((viewType, universalName, dimType)))
```

## Version
Availability: from Vectorworks 2023

## Category
* [Object Events](../Categories/Object%20Events.md)
