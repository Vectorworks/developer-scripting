# SetVisionMapping

## Description
Sets the mapping of the lighting device fields from Vectorworks to Vision.

```pascal
PROCEDURE SetVisionMapping(
				color    : STRING;
				universe : STRING;
				gobo     : STRING;
				name     : STRING;
				channel  : STRING);
```

```python
def vs.SetVisionMapping(color, universe, gobo, name, channel):
    return None
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
SetVisionMapping('Example', 'Example', 'Example', 'Example', 'Example');
```
```python
import vs

# Sets the mapping of the lighting device fields from Vectorworks to Vision.
color = 'Example'
universe = 'Example'
gobo = 'Example'
name = 'Example'
channel = 'Example'

vs.SetVisionMapping(color, universe, gobo, name, channel)
```

## Version
Availability: from Vectorworks 2018

## Category
* [Spotlight](../Categories/Spotlight.md)
