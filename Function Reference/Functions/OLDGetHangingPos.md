# OLDGetHangingPos

## Description
Returns handle of the Hanging Position where the specified load is attached.

```pascal
FUNCTION OLDGetHangingPos(
				handle    : HANDLE;
				loadIndex : INTEGER): HANDLE;
```

```python
def vs.OLDGetHangingPos(handle, loadIndex):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|handle|HANDLE|   |
|loadIndex|INTEGER|   |

## Examples
```pascal
BEGIN
	hPosition := OLDGetHangingPos( ghParm, 0 );

					SetRField (ghParm, kPIOName, 'ProjStand', Concat(GetRField(ghParm,kPIOName,'__DefaultStand')));
						SetRField (ghParm, kPIOName, '__StandSymbol', Concat(GetRField(ghParm,kPIOName,'ProjStand')));
					END;
			END;
	hAssocRigObjScreen := OLDGetHangingPos (ghParm,kLoadScreenIndex);
	IF hAssocRigObjScreen <> NIL THEN AssocPosNameScreen := AttachedPosData(hAssocRigObjScreen);
	IF (AssocPosNameScreen <> '') THEN SetRField(ghParm, kPIOName,'Position',Concat(AssocPosNameScreen));
END;

BEGIN
	hangPosProj := OLDGetHangingPos( ghParm, kLoadProjector1Index );
```
```python
import vs

# Returns handle of the Hanging Position where the specified load is attached.
handle = vs.FSActLayer()  # handle to the first selected object on the active layer
loadIndex = 1

objHandle = vs.OLDGetHangingPos(handle, loadIndex)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2019

## Category
* [Truss Analysis](../Categories/Truss%20Analysis.md)
