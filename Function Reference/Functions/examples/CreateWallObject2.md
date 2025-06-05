#### VectorScript

```pascal
// filepath: d:\Engineering\developer-scripting\Function Reference\Functions\examples\CreateWallObject2.md
DoubLines(6");
AddCavity(TRUE,1",2",2);
Wall(0,1,9,1);
ClearCavities;
Wall(0,2,11,2);
{creates a wall with a cavity, then creates a wall without a cavity}
```

#### Python

```python
// filepath: d:\Engineering\developer-scripting\Function Reference\Functions\examples\CreateWallObject2.md
vs.DoubLines(6)
vs.AddCavity(True,1,2,2)
vs.Wall(0,1,9,1)
vs.ClearCavities()
vs.Wall(0,2,11,2)
# {creates a wall with a cavity, then creates a wall without a cavity}
```
