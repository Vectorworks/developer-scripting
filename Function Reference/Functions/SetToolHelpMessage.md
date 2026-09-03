# SetToolHelpMessage

## Description
Sets the Tool Bar Help Text by new standard - Tool Name[: Tool Mode][. Brief usage advice.].

```pascal
PROCEDURE SetToolHelpMessage(
				modeText        : STRING;
				descriptionText : STRING);
```

```python
def vs.SetToolHelpMessage(modeText, descriptionText):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|modeText|STRING|The text that will be showed like as a name of the mode.|
|descriptionText|STRING|The text that will be showed like as an advice text.|

## Examples
```pascal
	SetToolHelpMessage( modeName, '' );
END;

	SetToolHelpMessage( helpString, '' );
END;

{set the default help string}
SetToolHelpMessage( '', GetPlugInString(5003) );
```
```python
import vs

# Sets the Tool Bar Help Text by new standard - Tool Name[: Tool Mode][.
modeText = 'Example text'
descriptionText = 'Example text'

vs.SetToolHelpMessage(modeText, descriptionText)
```

## Version
Availability: from Vectorworks 2013

## Category
* [User Interactive](../Categories/User%20Interactive.md)
