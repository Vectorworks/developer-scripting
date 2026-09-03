# SetClUseTexture

## Description
Toggles the document setting for using the texture attributes of the specified class at object creation.

```pascal
PROCEDURE SetClUseTexture(
				className : STRING;
				use       : BOOLEAN);
```

```python
def vs.SetClUseTexture(className, use):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|className|STRING|Name of class.|
|use|BOOLEAN|Use texture attributes on-off setting.|

## Remarks
Sets whether the class texture attributes are used at object creation.

Respective 'Get' is under Textures: [GetClUseTexture](GetClUseTexture.md) .

## Examples
#### VectorScript ####
```pascal
SetClUseTexture('Proposed Roof',TRUE);
```
#### Python ####
```python

```

```pascal
		{Cannot create class _____; an object of type ____ with that name already exists.}
end else BEGIN
	NameClass(className);
	SetClUseGraphic(className, TRUE);
	SetClUseTexture(className, TRUE);
END;

		{Cannot create class _____; an object of that name already exists.}
end else BEGIN
	NameClass(className);
	SetClUseGraphic(className, TRUE);
	SetClUseTexture(className, TRUE);
END;

SetClUseTexture ((LocClassToApply),FALSE);
```
```python
# Cannot create class _____; an object of type ____ with that name already exists.
vs.NameClass( className )
vs.SetClUseGraphic( className, True )
vs.SetClUseTexture( className, True )
```

## See Also
VS Functions:
[GetClUseTexture](GetClUseTexture.md)

## Version
Availability: from VectorWorks8.0

## Category
* [Classes](../Categories/Classes.md)
