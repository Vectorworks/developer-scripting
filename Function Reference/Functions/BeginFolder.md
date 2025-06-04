# BeginFolder

## Description
Procedure BeginFolder creates a new symbol folder in a VectorWorks document. Any symbols or symbol folders created after the current call to BeginFolder will be nested inside the new symbol folder. A call to EndFolder will complete the creation of the symbol folder, which is then generated in the VectorWorks document.

To name the new symbol folder, precede BeginFolder with a call to NameObject.

```pascal
PROCEDURE BeginFolder;
```

```python
def vs.BeginFolder():
    return None
```

## Examples
==== VectorScript ====
```pascal
NameObject('Object Symbols');
BeginFolder;
BeginSym('Oval Symbols');
PenSize(14);
PenPat(2);
FillPat(1);
FillFore(0,0,0);
FillBack(65535,65535,65535);
PenFore(0,0,0);
PenBack(65535,65535,65535);
Oval(-1/4",1/4",3/4",-3/4");
EndSym;
EndFolder;
{creates the symbol folder 'Object Symbols', which contains a symbol}
```
==== Python ====
```python
vs.NameObject('Object Symbols')
vs.BeginFolder()
vs.BeginSym('Oval Symbols')
vs.PenSize(14)
vs.PenPat(2)
vs.FillPat(1)
vs.FillFore(0,0,0)
vs.FillBack(65535,65535,65535)
vs.PenFore(0,0,0)
vs.PenBack(65535,65535,65535)
vs.Oval(-1/4,1/4,3/4,-3/4)
vs.EndSym()
vs.EndFolder()
```

## Version
Availability: from All Versions

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
