# vsoADPBeginDimType

## Description
Begin providing the dimension type result for the Auto Dimension GetSupportedTypes (77) message sent to a Script object.

```pascal
PROCEDURE vsoADPBeginDimType(
				message       : LONGINT;
				universalName : DYNARRAY[] of CHAR;
				localizedName : DYNARRAY[] of CHAR);
```

```python
def vs.vsoADPBeginDimType(message, universalName, localizedName):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|message|LONGINT|   |
|universalName|DYNARRAY[] of CHAR|   |
|localizedName|DYNARRAY[] of CHAR|   |

## Examples
```pascal
vsoADPBeginDimType(1, universalName, localizedName);
```
```python
import vs

# Begin providing the dimension type result for the Auto Dimension
# GetSupportedTypes (77) message sent to a Script object.
message = 'Hello Vectorworks'
universalName = 'Example'
localizedName = 'Example'

vs.vsoADPBeginDimType(message, universalName, localizedName)
```

## Version
Availability: from Vectorworks 2023

## Category
* [Object Events](../Categories/Object%20Events.md)
