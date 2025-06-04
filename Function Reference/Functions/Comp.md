# Comp

## Description
Returns the components of a comparison of two vectors.

The vector component of v1 along v2 in v3, and the vector component of v1 orthogonal to v2 in v4.

```pascal
PROCEDURE Comp(
				v1     : VECTOR;
				v2     : VECTOR;
				VAR v3 : VECTOR;
				VAR v4 : VECTOR);
```

```python
def vs.Comp(v1, v2):
    return (v3, v4)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|v1|VECTOR|Comparison vector 1.|
|v2|VECTOR|Comparison vector 2|
|v3|VECTOR|Component of vector 1 along vector 2|
|v4|VECTOR|Component of vector 1 orthogonal to vector 2.|

## Remarks
([[User:CBM-c-|_c_]], 2022.01.19) In VS Python the tuples v1 and v2 must be 3-dimensional, or the function will return gibberish.

([[User:CBM-c-|_c_]], 2010 Dec. 22) See graphical representation of how '''Comp''' works (click on the image to enlarge it):

[[File:C_MathVectorComp.png|200px ]]

## Examples
#### VectorScript ####
```python
PROCEDURE Example;
VAR
    v1, v2, v3, v4 : VECTOR;
BEGIN
    v1.x := 12; v1.y := 1; { vector can be bidimensional without failure }
    v2.x := 3; v2.y := 15;
    Comp( v1, v2, v3, v4 );
    Message(Concat( v3, Chr(13), v4 ));
END;
Run(Example);
```
#### Python ####
```python
v1 = (12, 1, 0) # 3-dimensional tuples
v2 = (3, 15, 0)
v3, v4 = vs.Comp( v1, v2 )
vs.Message(str(v3) + '\r' + str(v4))
```

## Version
Availability: from All Versions

## Category
* [Math - Vectors](../Categories/Math%20-%20Vectors.md)
