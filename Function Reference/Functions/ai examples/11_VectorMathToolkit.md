# 11. 2D Vector Math Toolkit

## Description
A compact set of pure-Python 2D vector helpers that the other algorithmic
examples in this folder rely on: add, subtract, scale, dot, 2D scalar cross,
length, normalise, perpendicular and rotate. The functions all take and return
plain `(x, y)` tuples so they interoperate with the point tuples that Vectorworks
returns from calls like `vs.GetPolyPt`.

After defining the toolkit the script produces a visual "cheat sheet": a source
vector and its rotated / perpendicular / normalised versions, each drawn as an
arrow rooted at a common origin.

## What This Demonstrates
- A reusable, dependency-free 2D vector library that you can paste into any
  Vectorworks Python script
- Drawing arrows on top of `MoveTo` / `LineTo`
  ([`MoveTo`](../MoveTo.md), [`LineTo`](../LineTo.md))
- Labelling geometry with [`CreateText`](../CreateText.md)
  and [`TextOrigin`](../TextOrigin.md)

## Python Script
```python
import math
import vs

# -------------------------------------------------------------------------
# 2D vector helpers. Every function takes and returns (x, y) tuples so the
# same values can be handed straight to vs.MoveTo/LineTo/Add2DVertex.
# -------------------------------------------------------------------------
def v_add(a, b):        return (a[0] + b[0], a[1] + b[1])
def v_sub(a, b):        return (a[0] - b[0], a[1] - b[1])
def v_mul(a, s):        return (a[0] * s,    a[1] * s)
def v_neg(a):           return (-a[0], -a[1])

def v_dot(a, b):        return a[0] * b[0] + a[1] * b[1]

# 2D scalar cross: positive if b is CCW of a, negative if CW.
def v_cross(a, b):      return a[0] * b[1] - a[1] * b[0]

def v_len(a):           return math.hypot(a[0], a[1])

def v_norm(a):
    """Return a with length 1; (0, 0) is returned unchanged."""
    L = v_len(a)
    return (a[0] / L, a[1] / L) if L > 1e-12 else (0.0, 0.0)

def v_perp(a):
    """Left perpendicular: rotate 90 deg CCW."""
    return (-a[1], a[0])

def v_rot(a, radians):
    """Rotate `a` by `radians` counter-clockwise."""
    c = math.cos(radians)
    s = math.sin(radians)
    return (a[0] * c - a[1] * s, a[0] * s + a[1] * c)

def v_angle(a):
    """Angle from +X axis in degrees, in the range (-180, 180]."""
    return math.degrees(math.atan2(a[1], a[0]))

def v_dist(a, b):       return v_len(v_sub(a, b))

# -------------------------------------------------------------------------
# Small visual helper: draw an arrow from `origin` to `origin + vec`.
# -------------------------------------------------------------------------
def draw_arrow(origin, vec, label=''):
    tip = v_add(origin, vec)
    vs.MoveTo(origin[0], origin[1])
    vs.LineTo(tip[0], tip[1])

    # Arrowhead: two short back-strokes rotated +/-25 deg from the shaft.
    head_len = 0.15 * v_len(vec)
    if head_len > 0:
        back = v_mul(v_norm(vec), -head_len)
        left  = v_rot(back,  math.radians(25))
        right = v_rot(back, -math.radians(25))
        vs.MoveTo(tip[0], tip[1])
        vs.LineTo(tip[0] + left[0],  tip[1] + left[1])
        vs.MoveTo(tip[0], tip[1])
        vs.LineTo(tip[0] + right[0], tip[1] + right[1])

    if label:
        vs.TextOrigin(tip[0] + 0.05, tip[1] + 0.05)
        vs.CreateText(label)


def main():
    origin = (0.0, 0.0)
    v = (2.0, 1.0)

    draw_arrow(origin, v,                          'v')
    draw_arrow(origin, v_perp(v),                  'perp(v)')
    draw_arrow(origin, v_rot(v, math.radians(45)), 'rot(v, 45deg)')
    draw_arrow(origin, v_mul(v_norm(v), 1.5),      '1.5 * norm(v)')

    # Dot product of two vectors laid at (5, 0) so nothing overlaps.
    a = (1.5, 0.5)
    b = (0.5, 1.4)
    base = (5.0, 0.0)
    draw_arrow(base, a, 'a')
    draw_arrow(base, b, 'b')

    dot = v_dot(a, b)
    cross = v_cross(a, b)
    vs.TextOrigin(base[0], base[1] - 0.6)
    vs.CreateText('a . b = ' + vs.Num2Str(3, dot)
                  + '    a x b = ' + vs.Num2Str(3, cross))

main()
```

## Key VectorScript Functions Used
- [`MoveTo`](../MoveTo.md), [`LineTo`](../LineTo.md)
- [`TextOrigin`](../TextOrigin.md), [`CreateText`](../CreateText.md)
- [`Num2Str`](../Num2Str.md)
- (see [`Norm`](../Norm.md), [`Vec2Ang`](../Vec2Ang.md) and [`Ang2Vec`](../Ang2Vec.md) for the built-in equivalents that operate on 3D `VECTOR` values)
