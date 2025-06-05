## VectorScript

```pascal
{ Create a new hatch and add it to the resource list. }
hatchName := 'Hatch-1';
BeginVectorFillN(hatchName, true, false, 0);
AddVectorFillLayer(0, 0, 1, 1, .25, -.25, .7, 3, 255);
EndVectorFill;
newHatch := GetObject(hatchName);
index := AddResourceToList(listID, newHatch);
```

## Python

```python
def Example():
	#{ Create a new hatch and add it to the resource list. }
	kHatch = 66
	kDefHatchFolder = 105
	hatchName = 'Hatch-1'

	listID, numItems = vs.BuildResourceList(kHatch, kDefHatchFolder, '')
	vs.BeginVectorFillN(hatchName, True, False, 0)
	vs.AddVectorFillLayer(0, 0, 1, 1, .25, -.25, .7, 3, 255)
	vs.EndVectorFill()
	newHatch = vs.GetObject(hatchName)
	index = vs.AddResourceToList(listID, newHatch)
Example()
```
