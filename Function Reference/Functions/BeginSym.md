# BeginSym

## Description
Procedure BeginSym creates a new symbol definition in a VectorWorks document. 

Any objects created after a call to BeginSym will be included in the symbol definition. A call to EndSym will complete the creation of the symbol, which is then generated in the VectorWorks document.

```pascal
PROCEDURE BeginSym(symbolName : STRING);
```

```python
def vs.BeginSym(symbolName):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|symbolName|STRING|Name of the new symbol.|

## Remarks
Note: normally SetOriginAbsolute(0,0) should be called before calling this. The user origin is used as the insertion point for the symbol, but it may be out of bounds, in which case the symbol is still created but the center of the document is used instead for the insertion point.


BeginSym deselects all objects on the active layer (VW 13, 83388). Be aware of your handles created after that.

## Examples
#### VectorScript ####
```pascal
BeginSym('Window');
Rect(-5'-11",-1",-2'-0",-5'-11");
Rect(-5'-8 3/4",-2 1/4",-2'-2 1/4",-2'-10");
Rect(-5'-8 3/4",-3'-1 3/4",-2'-2 1/4",-5'-9");
Rect(-4'-7",-2'-7 3/4",-3'-3 1/2",-2'-9 1/2");
MoveTo(-5'-11",-3'-0");
LineTo(-2'-0",-3'-0");
EndSym;
```
#### Python ####
```python
vs.BeginSym('WindowNew')
vs.Rect(-5*12 -11,-1*12,-2*12,-5*12 -11)
vs.Rect(-5*12 -8 - 3/4,-2*12 + 1/4,-2*12 -2 - 1/4,-2*12 -10)
vs.Rect(-5*12 -8 - 3/4,-3*12 - 1 - 3/4,-2*12 -2 - 1/4,-5*12 - 9)
vs.Rect(-4*12 -7,-2*12 -7 - 3/4,-3*12 - 3 - 1/2,-2*12 - 9 - 1/2)
vs.MoveTo(-5*12 - 11,-3*12)
vs.LineTo(-2*12,-3*12)
vs.EndSym()
```

## Version
Availability: from All Versions

## Category
* [Objects - Symbols](../Categories/Objects%20-%20Symbols.md)
