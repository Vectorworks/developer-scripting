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

## Version
Availability: from Vectorworks 2023

## Category
* [Object Events](../Categories/Object%20Events.md)
