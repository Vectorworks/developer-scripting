# SetConstrain

## Description
Procedure SetConstrain sets the active drawing constraints for the document. Each constraint is represented by an ASCII character identifier; these characters are assembled into a string which determines the constraints to be activated.

**VectorWorks Constraint Identifiers**

| Constraint           | Identifier |
|----------------------|------------|
| Snap To Grid         | A          |
| Snap To Objects      | Q          |
| Constrain Angle      | S          |
| Snap Intersection    | W          |
| Smart Points         | D          |
| Snap To Distance     | E          |
| Smart Edge           | F          |
| Constrain Tangent    | R          |

```pascal
PROCEDURE SetConstrain(str : STRING);
```

```python
def vs.SetConstrain(str):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|str|STRING|Constraint constant string.|

## Examples
#### VectorScript ####
```pascal
SetConstrain('QD');

{activates the snap objects and smart point constraints and deactivates the others}
```
#### Python ####
```python

```

## Version
Availability: from All Versions

## Category
* [Document Settings](../Categories/Document%20Settings.md)
