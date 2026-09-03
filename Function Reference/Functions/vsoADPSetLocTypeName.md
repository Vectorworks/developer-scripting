# vsoADPSetLocTypeName

## Description
Provide the localized type name result for the Auto Dimension GetLocalizedTypeName (76) message sent to a Script object.

```pascal
PROCEDURE vsoADPSetLocTypeName(
				message       : LONGINT;
				localizedName : DYNARRAY[] of CHAR);
```

```python
def vs.vsoADPSetLocTypeName(message, localizedName):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|message|LONGINT|   |
|localizedName|DYNARRAY[] of CHAR|   |

## Examples
```pascal
vsoADPSetLocTypeName(1, localizedName);
```
```python
import vs

# Provide the localized type name result for the Auto Dimension
# GetLocalizedTypeName (76) message sent to a Script object.
message = 'Hello Vectorworks'
localizedName = 'Example'

vs.vsoADPSetLocTypeName(message, localizedName)
```

## Version
Availability: from Vectorworks 2023

## Category
* [Object Events](../Categories/Object%20Events.md)
