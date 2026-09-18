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

## Examples
```pascal
vsoADPGetUniTypeName(1, universalName);
```
```python
import vs

# Retrieve the universal type name parameter from the Auto Dimension
# GetLocalizedTypeName (76) message sent to a Script object.
message = 'Hello Vectorworks'

result = vs.vsoADPGetUniTypeName(message)
```

## Version
Availability: from Vectorworks 2023

## Category
* [Object Events](../Categories/Object%20Events.md)
