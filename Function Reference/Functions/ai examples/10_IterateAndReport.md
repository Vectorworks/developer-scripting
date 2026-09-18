# 10. Iterate the Drawing and Report a Summary

## Description
Walks the objects on the active layer, counts them by object-type code, and
totals up their bounding-box area. This is the same pattern used in the site-
audit and inventory scripts (`VA Redline Auditor.px`, `Inventory Report.px`).
Two techniques are shown side-by-side:

* the callback-based [`ForEachObject`](../ForEachObject.md)
  approach, and
* an explicit [`FObject`](../FObject.md) /
  [`NextObj`](../NextObj.md) walk that lets you break early.

## What This Demonstrates
- Building a criteria string and passing it to
  [`ForEachObject`](../ForEachObject.md)
- Filtering by type with numeric type codes returned by
  [`GetTypeN`](../GetTypeN.md)
- Reading each object's bounding box with
  [`GetBBox`](../GetBBox.md)
- Walking the drawing list manually with
  [`FObject`](../FObject.md) /
  [`NextObj`](../NextObj.md)

## Python Script
```python
import vs

# A subset of common object type codes (see ObjsType.py in Common/Includes).
# The full list is documented in Appendix E of the reference.
kTypeNames = {
    2:  'Line',
    3:  'Rectangle',
    4:  'Oval',
    5:  'Polygon',
    6:  'Arc',
    10: 'Text',
    15: 'Symbol Instance',
    21: 'Polyline',
    24: 'Extrude',
    31: 'Layer',
    34: 'Sweep',
    47: 'Locus',
    83: 'Wall',
    86: 'Plug-in Object',
}

# We accumulate into module-level dicts because ForEachObject callbacks can't
# return values.
_counts = {}
_area_by_type = {}


def _bbox_area(h):
    """Return width*depth of the object's bounding box, or 0 if unavailable."""
    p1, p2 = vs.GetBBox(h)
    width  = abs(p2[0] - p1[0])
    depth  = abs(p2[1] - p1[1])
    return width * depth


def _tally(h):
    """ForEachObject callback: increment counters for this object."""
    t = vs.GetTypeN(h)
    label = kTypeNames.get(t, 'type ' + str(t))
    _counts[label] = _counts.get(label, 0) + 1
    _area_by_type[label] = _area_by_type.get(label, 0.0) + _bbox_area(h)


def SummarizeActiveLayer():
    """Iterate the active layer once and dump a summary to the message bar."""
    _counts.clear()
    _area_by_type.clear()

    # Criteria: everything visible on the active layer.
    criteria = "(L=" + "'" + vs.GetLName(vs.ActLayer()) + "'" + ")"
    vs.ForEachObject(_tally, criteria)

    if not _counts:
        vs.Message('Active layer is empty.')
        return

    # Build a compact single-line report.
    parts = []
    for label in sorted(_counts.keys()):
        parts.append(label + ': ' + str(_counts[label])
                     + ' (area=' + vs.Num2Str(2, _area_by_type[label]) + ')')
    vs.Message(' | '.join(parts))


def CountFirstThreeManually():
    """Show how to walk the list with FObject / NextObj to bail out early."""
    h = vs.FObject()
    seen = 0
    while h is not None and seen < 3:
        vs.SelectObj('(SEL=FALSE)')   # no-op safety
        vs.SetSelect(h)               # highlight the first three
        h = vs.NextObj(h)
        seen += 1


def main():
    SummarizeActiveLayer()
    CountFirstThreeManually()

main()
```

## Key VectorScript Functions Used
- [`ForEachObject`](../ForEachObject.md), [`ForEachObjectInLayer`](../ForEachObjectInLayer.md)
- [`FObject`](../FObject.md), [`NextObj`](../NextObj.md)
- [`GetTypeN`](../GetTypeN.md), [`GetBBox`](../GetBBox.md)
- [`ActLayer`](../ActLayer.md), [`GetLName`](../GetLName.md)
- [`SetSelect`](../SetSelect.md)
- [`Num2Str`](../Num2Str.md), [`Message`](../Message.md)
