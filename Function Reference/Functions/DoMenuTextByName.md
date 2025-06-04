# DoMenuTextByName

## Description
Calls the specified VectorWorks menu command item.

If the item is part of a VectorWorks menu chunk, pass the position of the item within the chunk as the second parameter. For menu items that are not part of a chunk, pass 0 as the second parameter.

Note: DoMenuTextByName uses the internal VectorWorks menu item name to reference the menu command, and calls to this procedure will work on localized (international) versions of VectorWorks without modification. Note also that when calling VS plug-ins, you have to use the filename (which could be different from the internal plug-in name).

A table listing DoMenuTextByName values can be found in the [[VS:Function Reference Appendix#Appendix H - DoMenuTextByName Constants| VectorScript Appendix]].

```pascal
PROCEDURE DoMenuTextByName(
				subMenu : STRING;
				index   : INTEGER);
```

```python
def vs.DoMenuTextByName(subMenu, index):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|subMenu|STRING|Menu item  selector.|
|index|INTEGER|Menu chunk item position (range of 1 -  n).|

## Remarks
If a plug-in command (.vsm) uses global variables that are being used by various subroutines and also uses parameters, the command will not work if it is called using DoMenuTextByName. The global variables are not maintaining their values and are being reset to 0, NIL, False, etc. as if they were local variables in each subroutine. This is in the bug list.

([[User:CBM-c-|_c_]], 2016.02.17): This is not operational when used from the regen event (kParametricRecalculate) or set up event (kObjOnInitXProperties) of plug-in objects. But can be used outside. To be noted that other view routines behave the same. the Plug-in regeneration environment is isolated.

([[User:CBM-c-|_c_]], 2007.03.18): DoMenuTextByName('Classes', 0); is not valid any longer (from VW 12.5+),
use DoMenuTextByName('Organization', 0); instead. This call will fail if the specified item is not present in the workspace.

## Examples
==== VectorScript ====
```pascal
PROCEDURE DoMenuTextByNameExample;
BEGIN
DoMenuTextByName('Print',0); {calls the print dialog}
DoMenuTextByName('Standard Views',8); {sets view to right isometric}
END;
RUN(DoMenuTextByNameExample);
```
==== Python ====
```python
def DoMenuTextByNameExample():
	vs.DoMenuTextByName('Print',0); #{calls the print dialog}
	vs.DoMenuTextByName('Standard Views',8); #{sets view to right isometric}
DoMenuTextByNameExample()
```

## Version
Availability: from MiniCAD 5.0

## Category
* [Command](../Categories/Command.md)
