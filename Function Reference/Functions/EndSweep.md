# EndSweep

## Description
Procedure EndSweep completes the definition of a sweep object within a VectorWorks document. On calling EndSweep, the object is created in the document from the preceding object creation calls.

It is recommended to call ResetOrientation3D after 3D object creations in order to ensure that the new 3D objects will draw properly.

```pascal
PROCEDURE EndSweep;
```

```python
def vs.EndSweep():
    return None
```

## Examples
#### VectorScript ####
```pascal
BeginSweep(#0,#360,#10,0');
Poly(3 1/4&quot;,-1/2&quot;,3 1/4&quot;,-1&quot;,2 3/4&quot;,-1&quot;,
2 1/4&quot;,-1/2&quot;,2 1/4&quot;,1&quot;,1 3/4&quot;,1 1/2&quot;,
-1 3/4&quot;,1 1/2&quot;,-2 1/4&quot;,1&quot;,-2 1/4&quot;,-1/2&quot;,
-2 3/4&quot;,-1&quot;,-3 1/4&quot;,-1&quot;,-3 1/4&quot;,-1/2&quot;,
-2 3/4&quot;,0&quot;,-2 3/4&quot;,1 1/2&quot;,-2 1/4&quot;,2&quot;,
2 1/4&quot;,2&quot;,2 3/4&quot;,1 1/2&quot;,2 3/4&quot;,0&quot;);
EndSweep;
```
#### Python ####
```python
vs.BeginSweep(0,360,10,0)
vs.Poly(3 + 1/4,-1/2,3 + 1/4,-1,2 + 3/4,-1,
2 + 1/4,-1/2,2 + 1/4,1,1 + 3/4,1 + 1/2,
-1 + 3/4,1 + 1/2,-2 + 1/4,1,-2 + 1/4,-1/2,
-2 + 3/4,-1,-3 + 1/4,-1,-3 + 1/4,-1/2,
-2 + 3/4,0,-2 + 3/4,1 + 1/2,-2 + 1/4,2,
2 + 1/4,2,2 + 3/4,1 + 1/2,2 + 3/4,0)
vs.EndSweep()
```

## Version
Availability: from All Versions

## Category
* [Objects - 3D](../Categories/Objects%20-%203D.md)
