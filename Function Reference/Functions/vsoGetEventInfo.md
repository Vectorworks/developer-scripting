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

## Examples
```pascal
BEGIN
	bsb := GetCustomObjectInfo(parmName, parmHand, parmRecordHand, wallHand);
	vsoGetEventInfo(theEvent, theButton);
	CASE theEvent OF
		kObjOnInitXProperties:
			BEGIN
				bsb := SetObjPropVS(kObjXPropHasUIOverride, TRUE);

BEGIN
{* Main program *}
	result := GetCustomObjectInfo(pluginName, pluginH, recordH, wallH);
	VSOGetEventInfo(eventID,eventMessage);
	CASE eventID OF
		 kObjOnInitXProperties:
			BEGIN
				result := SetObjPropVS(kObjXPropHasUIOverride,     TRUE);

BEGIN
	vsoGetEventInfo(theEvent, theButton);
	CASE theEvent OF
		kObjOnInitXProperties:
			BEGIN
				result := SetObjPropVS(kObjXPropSupportResourcePopup, TRUE);
```
```python
# Get event
theEvent, theButton	= vs.vsoGetEventInfo()

# Get event
theEvent, theEventData	= vs.vsoGetEventInfo()

# Get event
theEvent, theEventData	= vs.vsoGetEventInfo()
if theEvent == vs.kObjOnInitXProperties:
	ok	= vs.SetObjPropVS( vs.kObjXPropHasUIOverride, True )
	ok	= vs.SetObjPropVS( vs.kObjXHasCustomWidgetVisibilities, True )
```
See also in tutorials: [Plug-in with widgets, basic example (Python)](../../Common/Tasks/Parametrics/Plug-in%20with%20widget%20basic%20example.md)

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Object Events](../Categories/Object%20Events.md)
