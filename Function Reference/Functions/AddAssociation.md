# AddAssociation

## Description
Adds an object-to-object association.

```pascal
FUNCTION AddAssociation(
				ioOwnerObj  : HANDLE;
				inKind      : INTEGER;
				ioTargetObj : HANDLE):BOOLEAN;
```

```python
def vs.AddAssociation(ioOwnerObj, inKind, ioTargetObj):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|ioOwnerObj|HANDLE|   |
|inKind|INTEGER|   |
|ioTargetObj|HANDLE|   |

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
   {This script operates on any three parametric objects in the drawing.
     The objects must be named as required in GetObject Below.

   After the script has succeeded the following should be tested:
   1) deleting 'stairOne' deletes 'stairTwo'
   2) deleting 'stairTwo' deletes 'stairOne' and resets 'stairThree'
   
   Invoke Undo after each delete.}
CONST
   kOnDeleteDelete = 4; {Target object is deleted when owner is deleted.}
   kOnDeleteReset = 5;  {Target object is reset when owner is deleted.}
VAR
   obj1, obj2, obj3 :HANDLE;
   result :BOOLEAN;
BEGIN
   obj1 := GetObject('stairOne');
   obj2 := GetObject('stairTwo');
   obj3 := GetObject('stairThree');

   result := RemoveAssociation(obj1, kOnDeleteDelete, obj2);
   result := RemoveAssociation(obj2, kOnDeleteDelete, obj1);
   result := RemoveAssociation(obj2, kOnDeleteReset, obj3);

   result := AddAssociation(obj1, kOnDeleteDelete, obj2);
   result := AddAssociation(obj2, kOnDeleteDelete, obj1);
   result := AddAssociation(obj2, kOnDeleteReset, obj1);
END;
RUN(Example);
```
#### Python ####
```python
#   This script operates on any three parametric objects in the drawing.
#     The objects must be named as required in GetObject Below.
#
#   After the script has succeeded the following should be tested:
#   1) deleting 'stairOne' deletes 'stairTwo'
#   2) deleting 'stairTwo' deletes 'stairOne' and resets 'stairThree'
#   
#   Invoke Undo after each delete.

#CONST
kOnDeleteDelete = 4 # Target object is deleted when owner is deleted.
kOnDeleteReset = 5  # Target object is reset when owner is deleted.

obj1 = vs.GetObject('stairOne')
obj2 = vs.GetObject('stairTwo')
obj3 = vs.GetObject('stairThree')

result = vs.RemoveAssociation(obj1, kOnDeleteDelete, obj2)
result = vs.RemoveAssociation(obj2, kOnDeleteDelete, obj1)
result = vs.RemoveAssociation(obj2, kOnDeleteReset, obj3)

result = vs.AddAssociation(obj1, kOnDeleteDelete, obj2)
result = vs.AddAssociation(obj2, kOnDeleteDelete, obj1)
result = vs.AddAssociation(obj2, kOnDeleteReset, obj1)
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Object Events](../Categories/Object%20Events.md)
