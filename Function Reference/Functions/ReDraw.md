# ReDraw

## Description
Procedure ReDraw invokes a screen redraw of newly created objects in the active VectorWorks document. If new objects are to be manipulated using procedures which operate on selected objects, a call to ReDraw should precede the selected object routines to ensure that all new objects are correctly identified.

```pascal
PROCEDURE ReDraw;
```

```python
def vs.ReDraw():
    return None
```

## Remarks
If you use a .vsm or .vst to create a .vso, the object will not regen, even if you use redraw or redrawall. Try this at the very end of the vso script (assuming you have the vso set to regen on move):
HMove(parmHand,0,0);



Here's Julian's code for forcing a redraw...
```pascal
Procedure RegenGeometry;
VAR
CurrentPref : INTEGER;
BEGIN
CurrentPref := GetPrefInt(56);
SetPrefInt(56, CurrentPref / 2);
Layer(GetLName(ActLayer));
SetPrefInt(56, CurrentPref);
END;
```

## Version
Availability: from All Versions

## Category
* [Utility](../Categories/Utility.md)
