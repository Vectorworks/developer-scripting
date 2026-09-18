# Exp

## Description
Function Exp returns the value of e to the x, where e is the base of the natural logarithms and x is the specified value.

```pascal
FUNCTION Exp(v : REAL): REAL;
```

```python
def vs.Exp(v):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|v|REAL|   |

## Examples
```pascal
d1 := (kC + kB*Exp (-kA*gN1)) * pitchDia (gPitch, gN1);
d2 := (kC + kB*Exp (-kA*gN2)) * pitchDia (gPitch, gN2);
CDMin := (d1 + d2) / 2;

{* calculate the approximate of outside diameters of the sprockets, minimum center	*}
{* distance and minimum number of links								*}
gOD1 := (kC + kB*Exp (-kA*gN1)) * gD1;
gOD2 := (kC + kB*Exp (-kA*gN2)) * gD2;
minCD := (gOD1 + gOD2) / 2;
minNumLinks := getChainLength (gPitch, gN1, gN2, minCD) / gPitch;

{* calculate the approximate of outside diameters of the sprockets, minimum center	*}
{* distance and minimum number of links								*}
gOD1 := (kC + kB*Exp (-kA*gN1)) * gD1;
gOD2 := (kC + kB*Exp (-kA*gN2)) * gD2;
minCD := (gOD1 + gOD2) / 2;
minNumLinks := getChainLength (gPitch, gN1, gN2, minCD) / gPitch + 1;
```
```python
import vs

# Function Exp returns the value of e to the x, where e is the base of the
# natural logarithms and x is the specified value.
v = 1.0

value = vs.Exp(v)
vs.Message('Exp returned: ' + str(value))
```

## Version
Availability: from All Versions

## Category
* [Math - General](../Categories/Math%20-%20General.md)
