# GetVisionMapping

## Description
Gets the mapping of the lighting device fields from Vectorworks to Vision.

```pascal
PROCEDURE GetVisionMapping(
				VAR color    : STRING;
				VAR universe : STRING;
				VAR gobo     : STRING;
				VAR name     : STRING;
				VAR channel  : STRING);
```

```python
def vs.GetVisionMapping():
    return (color, universe, gobo, name, channel)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|color|STRING|   |
|universe|STRING|   |
|gobo|STRING|   |
|name|STRING|   |
|channel|STRING|   |

## Examples
```pascal
GetVisionMapping('Example', 'Example', 'Example', 'Example', 'Example');
```
```python
import vs

# Gets the mapping of the lighting device fields from Vectorworks to Vision.
color, universe, gobo, name, channel = vs.GetVisionMapping()
vs.Message('GetVisionMapping returned: ' + str((color, universe, gobo, name, channel)))
```

## Version
Availability: from Vectorworks 2018

## Category
* [Spotlight](../Categories/Spotlight.md)
