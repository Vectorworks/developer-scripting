# GetObjectTags

## Description
Lets the user query the list of Tags set on an object such as a Class,Layer or Resource.

```pascal
FUNCTION GetObjectTags(
				objHandle      : HANDLE;
				VAR outArrTags : ARRAY): BOOLEAN;
```

```python
def vs.GetObjectTags(objHandle):
    return (BOOLEAN, outArrTags)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objHandle|HANDLE|The handle to the object to query Tags from.|
|outArrTags|ARRAY|The output array of Tags queried from the object.|

## Examples
#### VectorScript ####
```pascal
Procedure Test;
var  h :Handle;
a :array[1..2] of string;

Begin
h:=FLayer;
GetObjectTags(h, a);
Message(Date(2,2),' ',a(1),' ',a(2));
end;

Run(Test);
```
#### Python ####
```python
h = vs.FLayer
b,t = vs.GetObjectTags(h)
vs.message(vs.Date(2,2), ' ', t[0], ' ', t[1])
```
VectorScript ====
<code lang="pas">
Procedure Test;
var  h :Handle;
a :array[1..2] of string;

Begin
h:=FLayer;
GetObjectTags(h, a);
Message(Date(2,2),' ',a(1),' ',a(2));
end;

Run(Test);</code>
#### Python ####
<code lang="py">
h = vs.FLayer
b,t = vs.GetObjectTags(h)
vs.message(vs.Date(2,2), ' ', t[0], ' ', t[1])
</code>

sample code by Pat Stanford

## Version
Availability: from Vectorworks 2019

## Category
* [General Edit](../Categories/General%20Edit.md)
