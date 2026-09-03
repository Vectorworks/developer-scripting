# SetClassN

## Description
Procedure SetClassN assigns a class to the referenced object.  <BR>
If the third parameter 'descIntoGroup' is set to true all objects within the group will receive the same class assignment as the group, <BR>
otherwise only the group itself will be affected.

```pascal
PROCEDURE SetClassN(
				h             : HANDLE;
				className     : STRING;
				descIntoGroup : BOOLEAN);
```

```python
def vs.SetClassN(h, className, descIntoGroup):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|className|STRING|Name of class to assign to object.|
|descIntoGroup|BOOLEAN|Assign the same class to all objects inside the group.|

## Examples
```python
{ select an object on drawing }
SetClassN(FSActLayer, 'Class Name-1', FALSE);
```

```pascal
			SetClUseTexture (gClassSpeakers,FALSE);
			SetClUseGraphic (gClassSpeakers,FALSE);
		END;
	wrkClsSpeakers := Concat(gClassSpeakers);
	SetClassN(hSymbolPartsGroup,gClassSpeakers,FALSE);
	IF ((gClassSpeakers<>'')&(gClassSpeakers<>' ')) THEN NameClass (Concat(ActClass));
END;
```
```python
import vs

# Procedure SetClassN assigns a class to the referenced object.
h = vs.FSActLayer()  # handle to the first selected object on the active layer
className = 'None'
descIntoGroup = True

vs.SetClassN(h, className, descIntoGroup)
```

## See Also
VS Functions:
[SetClass](SetClass.md)

## Version
Availability: from Vectorworks 2018

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
