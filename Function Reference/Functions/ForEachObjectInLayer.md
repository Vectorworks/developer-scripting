# ForEachObjectInLayer

## Description
Traverses through all objects according to specified search options and applies the specified action to each object.  The 'actionFunc' procedure should return false to continue with next object, or return true to stop the traversal.

**Table - ForEachObjectInLayer Selectors**

| Option                | Selector | Description                        |
|-----------------------|----------|------------------------------------|
| **Object Options**    |          |                                    |
| All objects           | 0        |                                    |
| Visible Objects only  | 1        |                                    |
| Selected Objects only | 2        |                                    |
| Unlocked objects only | 4        |                                    |
| **Traversal Options** |          |                                    |
| Traverse Shallow      | 0        |                                    |
| Traverse Groups       | 1        | Traverse inside groups             |
| Traverse Deep         | 2        | Traverse all containers (walls, extrudes, sweeps, etc) |
| **Layer Options**     |          |                                    |
| Current layer         | 0        |                                    |
| All layers            | 1        |                                    |
| Visible layers        | 2        |                                    |
| Editable layers       | 3        |                                    |
| Snappable layers      | 4        |                                    |

```pascal
PROCEDURE ForEachObjectInLayer(
				actionFunc   : FUNCTION;
				objOptions   : INTEGER;
				travOptions  : INTEGER;
				layerOptions : INTEGER);
```

```python
def vs.ForEachObjectInLayer(actionFunc, objOptions, travOptions, layerOptions):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|actionFunc|FUNCTION|Subroutine which performs operation on found objects.|
|objOptions|INTEGER|Object selection option index.|
|travOptions|INTEGER|Search options index.|
|layerOptions|INTEGER|Layer selection option index.|

## Remarks
Note that this will not descend into symdefs if it encounters a placed symbol. 

Be careful using this together with a call to "BeginSym": it deselects all selected objects on active layer (VW 13).

Should the variable type for actionFunc be "FUNCTION" instead of "PROCEDURE" in the declaration? Note that the this expects a Function that returns as boolean as shown in the example. The boolean should return true if you wish to stop processing further objects.

From the VS list:

Here is an interesting, yet disappointing, feature I just observed with ForEachObjectInLayer. Using v8.5.2 and ForEachObjectInLayer(FuncName, 4, 1, 0), I see that groups are NOT traversed unless they are LOCKED.
When Object Options is set to 4 (Locked Objects Only) AND Traversal Options is set to 1 (Traverse Groups) or 2 (Traverse Deep), FEOIL will not enter a group to look for LOCKED objects unless it too is LOCKED. Just another "feature" we need to program around.
When Traversal Options is set to 1, I would intuitively expect that GROUP objects would not be passed to FuncName, but the objects inside them would. I used the code below to select locked objects.

Best wishes,
Raymond

```pascal
********************
Procedure FEOIL;
{ Select all LOCKED objects in layer. Works in version 8.5.2,
but will not enter a group unless the group is locked, even
though the third parameter is set to 1 -> Traverse Groups. }

Function SetSelekt(Hnd: Handle) :Boolean;
Begin
SetSelect(Hnd);
SetSelekt := False;
End;            { SetSelekt }

BEGIN
DSelectObj(All);
ForEachObjectInLayer(SetSelekt, 4, 1, 0);
END;
Run(FEOIL);
```

## Examples
```pascal
PROCEDURE Example;

FUNCTION MakeItRed(h :HANDLE) :BOOLEAN;
VAR
r, g, b :LONGINT;
BEGIN
ColorIndexToRGB(7, r, g, b);
SetFillBack(h, r, g, b);
END;

BEGIN
ForEachObjectInLayer(MakeItRed, 2, 0, 4);
END;
RUN(Example);
```
Python:
```python
def MakeItRed(h):
    vs.SetFillBack( h, (65535, 0, 0) ) # red color - note that the values are 32-bit
    return False

vs.ForEachObjectInLayer( MakeItRed, 2, 0, 4 )
```

## Version
Availability: from VectorWorks 8.5

## Category
* [Utility](../Categories/Utility.md)
