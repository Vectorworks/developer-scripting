# vsoADPGetViewType

## Description
Retrieve the view type parameter from the Auto Dimension GetSupportedTypes (77) message sent to a Script object.

```pascal
PROCEDURE vsoADPGetViewType(
				message      : LONGINT;
				VAR viewType : INTEGER);
```

```python
def vs.vsoADPGetViewType(message):
    return viewType
```

## Parameters
|Name|Type|Description|
|---|---|---|
|message|LONGINT|   |
|viewType|INTEGER|   |

## Version
Availability: from Vectorworks 2023

## Category
* [Object Events](../Categories/Object%20Events.md)
