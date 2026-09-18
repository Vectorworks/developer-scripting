# vsoADPSetCatName

## Description
Sets the universal type name parameter and localized name parameter for the Auto Dimension GetDisplayCategoryName (79) message sent to a Script object.

```pascal
PROCEDURE vsoADPSetCatName(
				message       : LONGINT;
				universalName : DYNARRAY[] of CHAR;
				localizedName : DYNARRAY[] of CHAR);
```

```python
def vs.vsoADPSetCatName(message, universalName, localizedName):
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
vsoADPSetCatName(1, universalName, localizedName);
```
```python
import vs

# Sets the universal type name parameter and localized name parameter for the
# Auto Dimension GetDisplayCategoryName (79) message sent to a Script object.
message = 'Hello Vectorworks'
universalName = 'Example'
localizedName = 'Example'

vs.vsoADPSetCatName(message, universalName, localizedName)
```

## Version
Availability: from Vectorworks 2023

## Category
* [Object Events](../Categories/Object%20Events.md)
