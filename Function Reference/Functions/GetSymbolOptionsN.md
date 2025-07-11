# GetSymbolOptionsN

## Description
Returns default class, insert  options, and break options for the specified symbol. 


* Table - Symbol Insertion Options

| Category | Description | Constant Value |
|----------|-------------|----------------|
| Insertion Mode | Insert on Center Line | 0 |
| Insertion Mode | Insert on Edge | 1 |
| Break Mode | Full Break with Caps | 1 |
| Break Mode | Full Break No Caps | 2 |
| Break Mode | Half Break | 3 |
| Break Mode | No Break | 4 |

```pascal
PROCEDURE GetSymbolOptionsN(
				name           : STRING;
				VAR insertMode : INTEGER;
				VAR breakMode  : INTEGER;
				VAR className  : STRING);
```

```python
def vs.GetSymbolOptionsN(name):
    return (insertMode, breakMode, className)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|name|STRING|Name of symbol.|
|insertMode|INTEGER|Returns insertion mode of symbol.|
|breakMode|INTEGER|Returns break mode of symbol.|
|className|STRING|Default class of symbol.|

## Remarks
Gets the insertion options from the master symbol named &lt;name&gt;.

See [SetSymbolOptionsN](SetSymbolOptionsN.md).

Here's a way to get the left/right/center information for a symbol instance in a wall:
```pascal
PROCEDURE Example;
VAR
wallInstance, symInstance :HANDLE;
symLoc, wallBeg, wallEnd, relPt :VECTOR;

FUNCTION DoSomeThing(h :HANDLE) :BOOLEAN;
BEGIN
IF GetType(h) = 15 THEN BEGIN
symInstance := h;
wallInstance := GetParent(h);
END;
END;

BEGIN
symInstance := NIL;
ForEachObjectInLayer(DoSomeThing, 2, 2, 0);
IF symInstance <> NIL THEN BEGIN
GetSegPt1(wallInstance, wallBeg.x, wallBeg.y);
GetSegPt2(wallInstance, wallEnd.x, wallEnd.y);
GetSymLoc(symInstance, symLoc.x, symLoc.y);
relPt := RelativeCoords(symLoc, wallBeg, wallEnd);
IF relPt.y = 0 THEN Message('center') ELSE
IF relPt.y < 0 THEN Message('right') ELSE
IF relPt.y > 0 THEN Message('left');
END ELSE AlrtDialog('nil handle');
END;
RUN(Example);
```

## Version
Availability: from VectorWorks 8.5

## Category
* [Objects - Symbols](../Categories/Objects%20-%20Symbols.md)
