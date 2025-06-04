# Ang2Vec

## Description
Returns a 3-dimensional vector that is defined by the specified polar angle and length values.

```pascal
FUNCTION Ang2Vec(
				angleR : REAL;
				Length : REAL): VECTOR;
```

```python
def vs.Ang2Vec(angleR, Length):
    return VECTOR
```

## Parameters
|Name|Type|Description|
|---|---|---|
|angleR|REAL|The angle of the vector (in degrees).|
|Length|REAL|The length of the vector.|

## Remarks
([[User:CBM-c-|_c_]], 2022.01.20) The vector returned is always 3-dimensional whereby the last item is always 0: Pascal: {x, y, z}, Python: tuple (0.0, 0.0, 0.0)

## Examples
#### VectorScript ####
```python
Message( Ang2Vec(45, 1) ); { 3-dimensional vector whose z item is always 0 }
```
#### Python ####
```python
v = vs.Ang2Vec(45, 1)
vs.Message( str( v ) ) # 3-dimensional tuple whose last item is always 0
```

## Version
Availability: from All Versions

## Category
* [Math - Vectors](../Categories/Math%20-%20Vectors.md)
