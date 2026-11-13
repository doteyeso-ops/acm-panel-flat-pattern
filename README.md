# ACM panel flat patterns: blank size, notch, reveal and fold direction

The four numbers that decide whether a folded aluminium panel actually fits, and the one that surprises everybody.

A folded ACM panel is easy to draw and easy to get wrong. The drawing that gets sent to a fabricator is usually a 3D model of the finished part, while the machine needs a flat pattern with true-size geometry, one layer per operation and the fold direction marked. Between those two things sit four numbers that decide whether the panel fits.

## The numbers that decide it

- **Blanks per sheet is not what you think** — A 1200 x 900 pan comes out of a 2440 x 1220 sheet ONCE, at roughly 40% utilisation: 1200 across a 2440 leaves 1240 (not enough for a second), and 900 against 1220 leaves 320. The six-up figure people quote belongs to a 600 x 450 pan.
- **The notch is smaller than it looks** — A 25 mm notch on a 1250 mm blank is 2% of that edge. At drawing-card size it disappears, which is where shop-floor arguments start. Draw it enlarged and label it as enlarged.
- **Reveal and wear are not the notch** — The notch is where the corner folds; the reveal is the lap over the next panel; the wear strip is the return leg. They are cut, not folded, so they belong on their own layers - mix them and the router cuts your fold line.
- **Fold direction must be on the drawing** — Four folds, two directions. A flat pattern with no up/down marks is a coin flip on a pan brake, and a reversed fold is scrap.

## How to do it, in order

1. **Start from the visible face.** Panel size is the finished face, not the blank. Add the return legs and the reveal to get the blank, then check the blank against the sheet before pricing anything.
2. **Lay out operations, not shapes.** OUTLINE, VGROOVE, DRILL, WEEP, REVEAL as separate layers. Every layer is one operation at the machine; conflating them costs a second pass or a ruined sheet.
3. **Put the notch in real size, then zoom.** True-size geometry in the file, an enlarged detail on the presentation drawing, both labelled.
4. **Check the blank against the nest.** If the job is more than a few panels, nest the blanks before committing to a sheet count. Blank-per-sheet assumptions are where margin disappears.
5. **Export what the machine reads.** R2010 DXF, millimetres, true size, one layer per operation. A 3D model is for the architect; the flat pattern is for the router.

## Questions

**How many 1200 x 900 ACM pans fit on a 4x8 sheet?**

One, at about 40% utilisation. Two would need 2400 mm across a 2440 mm sheet (before trim and gaps) or 1800 mm against 1220 - neither fits. Six-up belongs to a 600 x 450 pan.

**Does the notch depth equal the return leg?**

No. The notch is cleared to the fold line so the corner closes; the return leg is the folded dimension. Conflating them is the commonest reason a corner opens up.

**What format does a fabricator need?**

Flat pattern DXF with true-size geometry and one layer per operation, plus a drawing that marks fold direction. OBJ/3DM are for design review, not cutting.

## If you would rather not do this by hand

NotchCad goes from panel size, return and thickness to a flat pattern, a nest, a cut list and machine files, with the numbers printed on the drawing. There is a free sample DXF - open it in your own CAM before forming an opinion.

→ **NotchCad** — https://notchcad.com?utm_source=github&utm_medium=repo&utm_campaign=acm-panel-flat-pattern

Written by the person who built NotchCad. The arithmetic above is the method; the tool automates it.

---

NotchCad · ACM panel design, nests and machine files · notchcad.com
