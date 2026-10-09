# Woodworking Technique Research — What the Pros Do Differently

Sourced from three videos analyzed via Gemini's native video read (cross-checked against known standard woodworking practice; a Chrome transcript pass was attempted but YouTube's player wouldn't buffer in this session, so treat this as single-source — solid content, just not double-verified):

1. **"Woodworking WITHOUT A Table Saw?? Here's How I Do It!"** — How I Do Things Woodworking
2. **"15 woodworking basics you should know"** — DIY Montreal
3. **"How to use a Router | Woodworking Guide for Beginners"** — 731 Woodworks

I picked these three specifically because they match your shop: no table saw, circular saw + track, router, drill, palm sander. Skipped the channels that lean on tools you don't have (table saw sleds, jointers, planers).

---

## The one-line takeaway

Every plan in your Woodworking folder is technically correct — the gap is precision *language*. Pro instructions spell out exactly which face rides the guide, exactly what the blade depth number is, and exactly which side of the pencil line loses material. Yours currently say "cut to length" and trust you to know the rest. That's fine for you now; it won't be reproducible by anyone else, and it's where small cumulative errors creep in even for you.

---

## Circular saw / track precision (no table saw)

| Technique | The specific rule |
|---|---|
| Blade depth | Set teeth to extend **workpiece thickness + 1/8"** past the material — not "however deep it goes." Formula, not eyeball. |
| Sightline | Don't trust the notch/gauge molded into the saw's baseplate — it's routinely off. Watch where the **teeth actually meet the pencil line**. |
| Kerf side | Mark an **X on the waste side** of your line and always cut so the blade removes the X side. Centering the blade *on* the line eats an extra ~1/8" and shorts the piece. |
| Continuous motion | Keep the saw moving at a steady pace start to finish. If you must stop: let the blade come to a **full stop**, back the saw up **~1/2" into the kerf**, restart at full speed, *then* resume forward. Stopping without backing up makes the blade wander or bind. |
| DIY zero-clearance guide | Glue a factory-edge plywood strip to a wider base strip, then trim the base flush with your own saw run down that edge — that trimmed edge becomes your exact "blade will land here" reference. Factory edge always faces the cut side. |
| Sheet goods support | Rest plywood/sheet stock on **rigid foam board**, not bare sawhorses, so the blade can cut 1/8" proud without binding, tearing the bottom face, or having the offcut drop and bind the blade. |
| Speed square crosscuts | For long dimensional lumber too unwieldy for a stop-block setup: hook the square's lip against the reference edge, run the saw's base flush against the square, and slide both together to the mark before cutting. |

## Fundamentals that don't make it into most DIY plans (including ours, currently)

| Rule | Why it matters for your builds |
|---|---|
| **Nominal ≠ actual lumber size.** A "2x4" is 1.5"×3.5". A "1x6" is 3/4"×5.5". | Every cut list needs to be built on actual dimensions or the whole plan is off from step one. |
| **Buy 10–15% extra lumber** on every project. | Covers defects, miscuts, and test cuts — cheap insurance against a mid-build supply run. |
| **Account for kerf when nesting multiple cuts from one board.** ~1/8" disappears per cut. | Matters most on your cut-heavy builds (chessboard, cribbage board, cornhole). |
| **Wood movement:** solid panels/tabletops need to float, not be screwed rigid to a frame. Use Z-clips, figure-8 fasteners, or elongated screw holes. | Directly relevant to the chair, side table, and any future tabletop — rigid mounting is exactly what splits solid wood over a season. |
| **Finish all faces, including undersides/unseen faces.** | One-sided sealing = uneven moisture absorption = warping later. Cheap to do at build time, annoying to fix after. |
| **Closed-grain hardwoods only for anything food-contact** (maple, walnut, cherry) — skip oak/ash (open pores trap liquid/bacteria). | Your walnut/maple keepsake box and any future cutting boards are already on the right track — worth stating explicitly so it's never assumed away. |
| **Sand in grit steps that roughly double, not skip** (e.g., 80→120→180→220). | You already call out 120→220; for rougher stock this adds a mid-step so scratches actually disappear. |
| **Never drive a screw into end grain/near an edge without a pilot hole + countersink.** | You already do pilot holes — worth also standardizing the countersink depth-stop callout. |

## Router technique

| Technique | The specific rule |
|---|---|
| Feed direction | **Counter-clockwise** around outside edges, **clockwise** around inside cutouts — always feeding *against* bit rotation. Going the other way ("climb cutting") lets the bit grab and yank the router out of control. |
| Depth per pass | Never take a routed cut to full depth in one pass. Cut in **1/8"–1/4" passes**, test the setup on a scrap offcut of the same species first. |
| Guiding without a router table | Clamped straightedge fence: measure the exact offset between the router base's edge and the bit's edge, then clamp the fence back that precise distance from your layout line. |
| Bit-to-task mapping | Straight bit → dados/grooves/rabbets. Roundover → eased edges. Chamfer → 45° bevel. Flush-trim (bearing-guided) → template duplication. |
| Tearout prevention | Back the exit edge with scrap, or rout end grain before face grain — that's usually where splintering starts. |

---

## Bottom line for your plans going forward

The fix isn't "learn more woodworking" — the recipes you're already generating are sound. It's **writing down the specifics pros say out loud but that get silently assumed in a written cut list**: blade depth as a formula, which side of the line is waste, the exact fence offset in inches, the feed-direction arrow, the wood-movement-safe attachment method. That's a documentation problem, not a skill problem, and it's exactly what I've updated in the woodworking-project-planner skill (see the file I'm sending alongside this).
