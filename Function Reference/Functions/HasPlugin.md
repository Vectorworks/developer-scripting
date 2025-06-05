# HasPlugin

## Description
Returns whether tool item or menu command is in current workspace.

```pascal
FUNCTION HasPlugin(
				itemUniversalName : STRING;
				VAR PaletteName   : STRING): BOOLEAN;
```

```python
def vs.HasPlugin(itemUniversalName):
    return (BOOLEAN, PaletteName)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|itemUniversalName|STRING|Universal name of the plug-in|
|PaletteName|STRING|If plug-in is a tool, and is found in the workspace, the name of the palette in which it is contained will be returned in this parameter|

## Remarks
In 2008, this only seems to work on plug-in objects and tools in the workspace.
The plug-ins have to _plug-ins_</i>_ (VectorScript or SDK features, not built-in objects or tools).
In other words, there has to be a file in the Plug-Ins folder associated with the feature.
And it doesn't work on plug-in menu commands.
In 12.5.3, it would work on menu commands, and the "paletteName" argument would be set to the menu group containing the item.

Example:
<code lang="pas">
PROCEDURE Example;
VAR
itemUniversalName :STRING;
paletteName :STRING;
result :BOOLEAN;
BEGIN
itemUniversalName := 'Spiral';
result := HasPlugin(itemUniversalName, paletteName);
AlrtDialog(Concat('result: ', result, Chr(13), 'paletteName: ', paletteName));
END;
RUN(Example);
</code>

## Version
Availability: from VectorWorks10.0

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
