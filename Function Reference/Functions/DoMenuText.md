# DoMenuText

## Description
Obsolete procedure.

```pascal
PROCEDURE DoMenuText(menuItem : STRING);
```

```python
def vs.DoMenuText(menuItem):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|menuItem|STRING|Menu item name.|

## Remarks
As of 9.0.0b7, DoMenuText will generate a runtime error if the user attempts to execute a main application menu item. It will continue to work wor worksheet menu items using the WS prefix until 10.0.0, when it will be removed completely. - PCP 12-21-2000

## See Also
VS Functions:
[DoMenuTextByName](DoMenuTextByName.md)

## Version
DoMenuText is obsolete as of VectorWorks8.0<P>


Availability: from MiniCAD4.0

## Category
* [Command](../Categories/Command.md)
