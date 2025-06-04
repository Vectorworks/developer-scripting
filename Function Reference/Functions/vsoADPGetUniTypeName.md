# vsoADPGetUniTypeName

## Description
Retrieve the universal type name parameter from the Auto Dimension GetLocalizedTypeName (76) message sent to a Script object.

```pascal
PROCEDURE vsoADPGetUniTypeName(
				message           : LONGINT;
				VAR universalName : DYNARRAY[] of CHAR);
```

```python
def vs.vsoADPGetUniTypeName(message):
    return universalName
```

## Parameters
|Name|Type|Description|
|---|---|---|
|message|LONGINT|   |
|universalName|DYNARRAY[] of CHAR|   |

## Version
Availability: from Vectorworks 2023

## Category
* [Object Events](../Categories/Object%20Events.md)
