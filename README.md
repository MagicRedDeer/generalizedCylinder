> Mirror of [iceanimations/generalizedCylinder](https://github.com/iceanimations/generalizedCylinder),
> published by the studio under EPL 2.0. Kept here for reference; the original repository is the canonical
> one.

# generalizedCylinder

Builds geometry along a curve, with the UVs adjusted so the tube does not pinch where the curve bends.

`generalizedCylinder.py` generates a tube along a NURBS curve with control over tube sections, then walks
the resulting rings and expands UVs ring by ring rather than letting Maya's default projection smear them.
`polyRope.py` sits on top of it and builds a rope: one centre cylinder plus side cylinders, each with its
own twist rate, width and sampling, so the strands spiral the way rope does.

Both are ordinary modelling tools with a rigging habit: `curveControlLocs.py` adds control locators along
the generated geometry, which is what a modeller or a rigger actually wants from a procedural tube.

## The modules

| File | Job |
|---|---|
| `src/generalizedCylinder.py` | Tube along a curve, UV expansion per ring |
| `src/polyRope.py` | Rope presets and option-var persistence |
| `src/curveControlLocs.py` | Control locators along the result |
| `src/interface.py`, `src/interface2.py` | Two generations of Qt window |

`interface.py` and `interface2.py` both existing is the honest state of a tool that was rewritten once
and the old file left in place.

## Authorship

27 commits between 2014 and 2021:

| Author | Commits |
|---|---|
| Qurban Ali | 17 |
| Talha Ahmed | 10 |

Qurban Ali wrote the majority of this one, including the rope generator. Mirrored as part of the toolbox,
not as an example of my code.

LICENSE
=======

Copyright 2021. Talha Ahmed. All rights reserved.

This work is licensed under the terms of Eclipse Public License - v 2.0.
For a copy see https://www.eclipse.org/org/documents/epl-2.0/EPL-2.0.txt
