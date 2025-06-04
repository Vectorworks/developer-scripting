# ForEachObjectInList

## Description
Processes all items in the specified list and and applies the specified action to each item.

{| class="wikitable_c"
|+ Table - ForEachObjectInList Selectors
! Option !! Selector !! Description
|-
! Colspan="3" | Object Options
|-
| All objects
| style="text-align:center"| 0
| 
|-
| Visible Objects only
| style="text-align:center"| 1
|  
|-
| Selected Objects only
| style="text-align:center"| 2
| 
|-
| Unlocked objects only
| style="text-align:center"| 4
| 
|-
! Colspan="3" | Traversal Options
|-
| Traverse Shallow
| style="text-align:center"| 0
|  
|-
| Traverse Groups
| style="text-align:center"| 1
| Traverse inside groups
|-
| Traverse Deep
| style="text-align:center"| 2
| Traverse all containers
(walls, extrudes, sweeps, etc)
|}

```pascal
PROCEDURE ForEachObjectInList(
				actionFunc  : FUNCTION;
				objOptions  : INTEGER;
				travOptions : INTEGER;
				list        : HANDLE);
```

```python
def vs.ForEachObjectInList(actionFunc, objOptions, travOptions, list):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|actionFunc|FUNCTION|Subroutine which performs operation on found objects.|
|objOptions|INTEGER|Object selection option index.|
|travOptions|INTEGER|Search options index.|
|list|HANDLE|Handle to first item in list.|

## Remarks
Be careful using this together with a call to [[VS:BeginSym]]: it deselects all selected objects on active layer (VW 13)

It seems that when you fill in a NIL Handle in the list Parameter, the ActionFunc will be executed on all the objects of the active layer (VW2011).

## Examples
{{TraverseObjectsInActiveLayer}}
```pascal
PROCEDURE Example;
CONST
pioName = 'Complex Window 2';
parameter = 'MeasureHeight';
value = 'Head of Window';

FUNCTION DoIt(h :HANDLE) :BOOLEAN;
BEGIN
h := FInSymDef(h);
SetRField(h, pioName, parameter, value);
END;

BEGIN
ForEachObjectInList(DoIt, 0, 0, FSymDef);
END;
RUN(Example);
```
Another example:
```pascal
PROCEDURE Example;
CONST
pioName = 'Window';
parameter = 'UPI';
value = '25.4';

FUNCTION DoIt(h :HANDLE) :BOOLEAN;
BEGIN
h := FInSymDef(h);
IF (h &lt;&gt; NIL) &amp; (GetType(h) = 86) &amp; (Eval(h, 'R IN [pioName])') &gt; 0) THEN BEGIN
SetRField(h, pioName, parameter, value);
END;
END;

BEGIN
ForEachObjectInList(DoIt, 0, 0, FSymDef);
END;
RUN(Example);
```
Python:
```pascal
pioName = 'Complex Window 2'
parameter = 'MeasureHeight'
value = 'Head of Window'

def DoIt(h):
    h := vs.FInSymDef(h);
    vs.SetRField(h, pioName, parameter, value);

vs.ForEachObjectInList(DoIt, 0, 0, vs.FSymDef);
```
==== Python ====
```python

```

## Version
Availability: from VectorWorks 8.5

## Category
* [Utility](../Categories/Utility.md)
