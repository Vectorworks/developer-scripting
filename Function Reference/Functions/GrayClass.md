# GrayClass

## Description
Sets the visibility of the specified class to grayed status.

```pascal
PROCEDURE GrayClass(className : STRING);
```

```python
def vs.GrayClass(className):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|className|STRING|Name of class.|

## Remarks
[sd 8/18/98]

## Examples
#### VectorScript ####
```pascal
GrayClass('Phase 2 Construction');
```
#### Python ####
```python
vs.GrayClass('Phase 2 Construction')
```

```pascal
tempVis := Abs (tempVis);
CASE tempVis OF
	0: ShowClass (ClassList (i));
	1: HideClass (ClassList (i));
	2: GrayClass (ClassList (i));
END;

						SetClUseGraphic (UserClassName, TmpClassInfo.UseAtCreation);
}
						{set the class visiblity for this class for this sheet}
						IF visibility = 'I' THEN HideClass (UserClassName)
						ELSE IF visibility = 'G' THEN GrayClass (UserClassName)
							ELSE ShowClass (UserClassName);
						IF visibility = 'A' THEN  actClass := UserClassName;
					END

{
writeln (' UserClassName = ',UserClassName ,'    visibility = ',visibility );
}
				IF visibility = 'I' THEN HideClass (UserClassName)
				ELSE IF visibility = 'G' THEN GrayClass (UserClassName)
				ELSE ShowClass (UserClassName);
				IF visibility = 'A' THEN tmpActClass := UserClassName;
			END;
```
```python
elif ( classVis_Curb == 2 ):
	vs.GrayClass( gCurb_Class )
```

## Version
Availability: from VectorWorks8.0

## Category
* [Classes](../Categories/Classes.md)
