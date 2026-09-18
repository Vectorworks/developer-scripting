# OLDMassDistRealToStr

## Description
Converts distributed mass real value to string and returns TRUE on success.

```pascal
FUNCTION OLDMassDistRealToStr(distrMassValue : REAL): STRING;
```

```python
def vs.OLDMassDistRealToStr(distrMassValue):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|distrMassValue|REAL|   |

## Examples
```pascal
	weightValue := Str2Num( GetRField( parmHand, parmName, kStrDistributedWeight ) );
	SetRField( parmHand, parmName, kStrDistrWeightStr, OLDMassDistRealToStr( weightValue ) );
END;

	SetRField (ghParm, kPIOName, 'DistWeight',Concat(OLDMassDistRealToStr(CalcDistWeight)));
	OLDSetLoadDataReal(ghParm,kDLDSelectorWeight,CalcDistWeight,0);
END

SetRField (H, kPIOName, 'DistWeight',Concat(OLDMassDistRealToStr(CalcDistWeight)));
```
```python
import vs

# Converts distributed mass real value to string and returns TRUE on success.
distrMassValue = 1.0

text = vs.OLDMassDistRealToStr(distrMassValue)
vs.Message('OLDMassDistRealToStr returned: ' + str(text))
```

## Version
Availability: from Vectorworks 2018

## Category
* [Truss Analysis](../Categories/Truss%20Analysis.md)
