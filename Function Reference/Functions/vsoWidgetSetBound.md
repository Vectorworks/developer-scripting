# vsoWidgetSetBound

```pascal
PROCEDURE vsoWidgetSetBound(
				widgetID_Popup  : LONGINT;
				widgetID_Offset : LONGINT;
				boundID         : LONGINT;
				isTop           : BOOLEAN;
				offsetLegPrm    : STRING);
```

```python
def vs.vsoWidgetSetBound(widgetID_Popup, widgetID_Offset, boundID, isTop, offsetLegPrm):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|widgetID_Popup|LONGINT|   |
|widgetID_Offset|LONGINT|   |
|boundID|LONGINT|   |
|isTop|BOOLEAN|   |
|offsetLegPrm|STRING|   |

## Examples
```pascal
{ set the architectural bound. }
vsoWidgetSetBound( kTopBoundArchitWidgetID, kTopOffsetArchitWidgetID, kTopBoundArchitID, TRUE  {top}, '' );
vsoWidgetSetBound( kBotBoundArchitWidgetID, kBotOffsetArchitWidgetID, kBotBoundArchitID, FALSE {top}, '' );

vsoWidgetSetBound( kTopBoundWidgetID, kTopOffsetWidgetID, kTopBoundID, true {top}, '' );
vsoWidgetSetBound( kBottomBoundWidgetID, kBottomOffsetWidgetID, kBottomBoundID, false {top}, '' );
```
```python
import vs

widgetID_Popup = 1
widgetID_Offset = 2
boundID = 3
isTop = True
offsetLegPrm = 'Example'

vs.vsoWidgetSetBound(widgetID_Popup, widgetID_Offset, boundID, isTop, offsetLegPrm)
```

## Version
Availability: from Vectorworks 2012

## Category
* [Object Events](../Categories/Object%20Events.md)
