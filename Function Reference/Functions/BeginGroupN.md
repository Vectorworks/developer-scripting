# BeginGroupN

## Description
May be used to create objects in an existing group by passing a group handle; if a handle initialized to NIL is passed a new group is created.

```pascal
PROCEDURE BeginGroupN(VAR groupHandle : HANDLE);
```

```python
def vs.BeginGroupN(groupHandle):
    return groupHandle
```

## Parameters
|Name|Type|Description|
|---|---|---|
|groupHandle|HANDLE|The group handle to be used; if handle is initialized to NIL a new group is created.|

## Remarks
[[User:CBM-c-| _c_]] 2021.02.24:

Be very careful with BeginGroupN, this won't automatically return NIL if empty. Used in Plug-in object it will crash VW upon attempting to use the common Group operation routines and the Group handle is not valid (Tested up to VW 2021 SP3).

```pascal
gr1 := NIL;
BeginGroupN(gr1);
EndGroup;
{ gr1 now unexpectedly is not NIL }
		
BeginGroup;
EndGroup;
gr2 := LNewObj;
{ this is NIL }

{ 
 IF gr1 <> NIL THEN
 	killer := CreateDuplicateObject(gr1, NIL); this hangs VW in pios }
		
{ 
IF gr1 <> NIL THEN
	killer := FInGroup(gr1); this causes VW to instantly quit in pios }

{ solution: make sure that the handle is valid adding some basic geometry that you might delete later }
BeginGroupN(gr1);
Locus(0, 0);
EndGroup;
```

## Examples
```pascal
BeginGroupN(groupHandle);
  Rect(-1,1,0.5,0);
EndGroup;
{ adds created rect to existing group }

groupHandle := nil;
BeginGroupN(groupHandle);
  Rect(-1,1,0.5,0);
EndGroup;
{ creates new group and adds created rect to created group }
```

## See Also
VS Functions:
[BeginGroup](BeginGroup.md) 
| [EndGroup](EndGroup.md)

## Version
Availability: from Vectorworks 2011

## Category
* [Objects - Groups](../Categories/Objects%20-%20Groups.md)
