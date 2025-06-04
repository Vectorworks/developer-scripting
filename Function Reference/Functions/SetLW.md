# SetLW

## Description
Procedure SetLW sets the line weight of the referenced object.

```pascal
PROCEDURE SetLW(
				h  : HANDLE;
				lw : INTEGER);
```

```python
def vs.SetLW(h, lw):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object|
|lw|INTEGER|Line weight to be applied to object (in mils).|

## Remarks
If you pass in the handle to a group, the objects within the group do not pickup the lineweight attribute. Compare this to the SetPenFore() procedure in which the objects within the group do pickup the colour attribute.

## Examples
#### VectorScript ####
```pascal
SetLW(ObjHd,12);
```
Better example:
```pascal
PROCEDURE LineWeightChange; 
{ (c) Petri Sakkinen 2008 }
CONST { substitute these with the required values }
oldWeight = 2; 
newWeight = 20;

PROCEDURE ChangeIt (h : HANDLE);
BEGIN 
SETLW(h, newWeight);
END; 

BEGIN
FOREACHOBJECT(ChangeIt, LW = oldWeight);
END; 

RUN(LineWeightChange);
```
And another example, from Pat Stanford:
```pascal
Procedure LW_Change;

{Set the FromLW and ToLW constants to the line weights (in mm)}

{That you want changed from and to}

{Vectorscript only handles lineweights in mils, so some trial } 
{and error may be required to determine the correct settings  } 
{March 13, 2008} {(c) 2008, Coviana, Inc - Pat Stanford pat@coviana.com} 
{Licensed under the GNU Lesser General Public License}

Const
FromLW = 0.05;
ToLW = 0.07;

Var
VFromLW, VToLW:Integer;

Procedure ChangeLW(H1:Handle);
Begin
If GetLW(H1)=VFromLW then SetLW(H1,VToLW);
end;

Begin
VFromLW := FromLW / 25.4 * 1000;
VToLW := ToLW / 25.4 * 1000;
{You may want to change the criteria on the next line if you }
{Don't want PIOs and Viewports to change}
ForEachObject(ChangeLW,(INSYMBOL &amp; INOBJECT &amp; INVIEWPORT &amp; (ALL))); 
end;

Run(LW_Change);
```
#### Python ####
```python

```

## Version
Availability: from All Versions

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
