# vstGetEventInfo

## Description
Gets the info on the current tool event. See vstEventsConstants.px for a list of events for tools.

```pascal
PROCEDURE vstGetEventInfo(
				VAR outAction   : LONGINT;
				VAR outMessage1 : LONGINT;
				VAR outMessage2 : LONGINT);
```

```python
def vs.vstGetEventInfo():
    return (outAction, outMessage1, outMessage2)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|outAction|LONGINT|Output parameter.|
|outMessage1|LONGINT|Output parameter.|
|outMessage2|LONGINT|Output parameter.|

## Remarks
Note that this procedure won't give back any information unless the tool is event-enabled. There does not seem to be a GUI method for enabling this; instead you'll have to open up the .vst file in a hex editor and change byte offset 144 (0x90) to "08". See image. (Thanks, Conrad!).

![RmTestTool.vst](files/RmTestTool.vst.jpg)

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Tool Events](../Categories/Tool%20Events.md)
