# vsoGetEventInfo

## Description
Returns the ID of the event in an event-enabled object. If the event was a button press, outEventData will indicate which button it was.

```pascal
PROCEDURE vsoGetEventInfo(
				VAR outObjEvent  : LONGINT;
				VAR outEventData : LONGINT);
```

```python
def vs.vsoGetEventInfo():
    return (outObjEvent, outEventData)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|outObjEvent|LONGINT|Output parameter.|
|outEventData|LONGINT|Output parameter.|

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Object Events](../Categories/Object%20Events.md)
