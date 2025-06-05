## VectorScript

```pascal
PROCEDURE Example;
VAR
objName :STRING;
objHand, recHand, wallHand :HANDLE;
colorIndexBefore, colorIndexAfter, pRed, pGreen, pBlue :INTEGER;
boo :BOOLEAN;
BEGIN
pRed := 65535;
pGreen := 0;
pBlue := 0;
IF GetCustomObjectInfo(objName, objHand, recHand, wallHand) THEN BEGIN
RGBToColorIndex(pRed, pGreen, pBlue, colorIndexBefore);
Rect(0, 0, 1, 1);
SetFillBack(LNewObj, colorIndexBefore);
IF SetCustomObjectColor(objHand, 1, colorIndexBefore) THEN BEGIN
boo := GetCustomObjectColor(objHand, 1, colorIndexAfter);
AlrtDialog(Concat('before: ', colorIndexBefore, Chr(13), 'after: ', colorIndexAfter));
END;
END;
END;
RUN(Example);
```

## Python

```python
def Example():
	pRed = 65535
	pGreen = 0
	pBlue = 0
	isValid, objName, objHand, recHand, wallHand = vs.GetCustomObjectInfo()
	if isValid:
		colorIndexBefore = vs.RGBToColorIndex(pRed, pGreen, pBlue)
		vs.Rect(0, 0, 1, 1)
		vs.SetFillBack(vs.LNewObj(), colorIndexBefore)
		isValid = vs.SetCustomObjectColor(objHand, 1, colorIndexBefore)
		if isValid:
			boo, colorIndexAfter = vs.GetCustomObjectColor(objHand, 1)
			vs.AlrtDialog(vs.Concat('before: ', colorIndexBefore, vs.Chr(13), 'after: ', colorIndexAfter))
Example()
```
