# CallToolWithMode

## Description
Activates the specified Vectorworks tool for a single use with the specified tool mode. After the tool has been used Vectorworks will revert back to the previously active tool.

```pascal
PROCEDURE CallToolWithMode(
				toolIndex  : INTEGER;
				modeGroup  : LONGINT;
				modeButton : LONGINT);
```

```python
def vs.CallToolWithMode(toolIndex, modeGroup, modeButton, callback):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|toolIndex|INTEGER|Vectorworks tool constant.|
|modeGroup|LONGINT|Index of the mode group|
|modeButton|LONGINT|Index of the button in the group.|
|callback|FUNCTION|Python only! A callback function that will be executed when the tool finishes.|

## Remarks
The python function requires an extra 'callback' parameter because python will not pause in the function, while the tool executes. The python will continue until the end of the script, and then the tool will be activated. The 'callback' function will be executed when the tool completes.
<code lang="py">
vs.CallToolWithMode( -221, 0, 0, any ) # 'Any' is and does absolutely nothing in prior to Vectorworks 2022 SP3
```

Changes the active tool to that specified by toolID. Waits until the user has executed the functionality of that tool, then switches back to the previously active tool &amp; returns.

## Version
Availability: from Vectorworks 2016

## Category
* [Utility](../Categories/Utility.md)
