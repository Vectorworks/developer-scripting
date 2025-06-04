# SetObjectTags

## Description
Lets the user set a list of Tags on an object such as a Class,Layer or Resource.

```pascal
FUNCTION SetObjectTags(
				objectHandle : HANDLE;
				arrTags      : ARRAY): BOOLEAN;
```

```python
def vs.SetObjectTags(objectHandle, arrTags):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHandle|HANDLE|The object to set Tags on.|
|arrTags|ARRAY|The arra of Tag Strings.|

## Examples
==== VectorScript ====
```pascal
Procedure Test;

Var		H1:		Handle;
		A1:		Array[1..2] of string;
		B1:		Boolean;
		
		
Begin
	H1:=FLayer;
	A1[1]:='Tag One';
	A1[2]:='Tag Two';
	B1:=SetObjectTags(H1,A1);
ENd;

Run(Test);
```
==== Python ====
```python
import vs

def SetTags():
	# List of tags i want to add
	l = ('Tag One','Tag Two')
	
	# Handle to the thing i want to add the label to
	h = vs.FLayer()
	
	# Function for setting the label
	vs.SetObjectTags(h, l)

SetTags()
```
VectorScript ====
<code lang="pas">
Procedure Test;

Var		H1:		Handle;
		A1:		Array[1..2] of string;
		B1:		Boolean;
		
		
Begin
	H1:=FLayer;
	A1[1]:='Tag One';
	A1[2]:='Tag Two';
	B1:=SetObjectTags(H1,A1);
ENd;

Run(Test);</code>
==== Python ====
<code lang="py">
import vs

def SetTags():
	# List of tags i want to add
	l = ('Tag One','Tag Two')
	
	# Handle to the thing i want to add the label to
	h = vs.FLayer()
	
	# Function for setting the label
	vs.SetObjectTags(h, l)

SetTags()
</code>


Sample VS by Pat Stanford
Sample PY by TWK, koenr, and Pat Stanford 4-12-24

## Version
Availability: from Vectorworks 2019

## Category
* [General Edit](../Categories/General%20Edit.md)
