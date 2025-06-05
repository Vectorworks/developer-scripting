==== VectorScript ====
```pascal
PROCEDURE Example;
VAR
h1, h2, h3 :HANDLE;
int :INTEGER;
BEGIN
DSelectAll; BeginXtrd(0, 1); CallTool(-203); h1 := FSActLayer; EndXtrd;
DSelectAll; BeginXtrd(0, 1); CallTool(-203); h2 := FSActLayer; EndXtrd;
int := AddSolid(h1, h2, h3);
END;
RUN(Example);
```

==== Python ====
```python
# No example provided
```
