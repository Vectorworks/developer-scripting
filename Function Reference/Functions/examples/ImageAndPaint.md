#### VectorScript

```pascal
PROCEDURE Example;
VAR
	hImage  : HANDLE;
	copyImage : HANDLE;
	paintHandle : HANDLE;
	importPt  : POINT;
BEGIN
	GetPt(importPt.x, importPt.y);
	hImage := ImportImageFile('D:\\Lenna.png', importPt.x, importPt.y );
	paintHandle := CreatePaintFromImage(hImage);
	copyImage := CreateImageFromPaint(paintHandle, 'Copy Image');
END;
RUN(Example);
```

#### Python

```python
def Example():	
	hImage = vs.ImportImageFile('D:\\Lenna.png', 10, 10 )
	paintHandle = vs.CreatePaintFromImage(hImage)
	copyImage = vs.CreateImageFromPaint(paintHandle , 'Copy Image')

Example()
```
