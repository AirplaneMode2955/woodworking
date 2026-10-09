---
name: "woodworking-project-planner"
description: "Turns a list of on-hand wood/materials into a buildable project. Use this skill whenever Airplane lists lumber, plywood, or shop scraps he has on hand and wants project ideas, or names a specific project he wants built from those materials. Also triggers on \"what can I build with\", \"give me a woodworking project\", \"I have some wood, what should I make\", \"plan out this build for me\", \"what wood should I buy for X\", or \"how much will this project cost.\" Produces a cut list, a wood species recommendation with reasoning, a total cost estimate, step-by-step instructions tailored to the tools on hand, and a copy-paste image prompt Airplane can drop into ChatGPT (or any image tool) himself to see a realistic render of the finished piece."
---

# Woodworking Project Planner

## Purpose
Turn a materials list into a real, buildable project: a specific plan, a cut list mapped to what's actually on hand, a wood species recommendation for anything still needing to be bought, a total cost estimate, build instructions written for the tools available, and a ready-to-paste image prompt for visualizing the finished piece.

## Airplane's shop (default — don't ask)
Airplane's standing tool set is a **circular saw, jig saw, router, drill/driver, palm sander, and wood glue**, plus basic hand tools (clamps, tape measure, speed square, sandpaper). He does **not** have a table saw, miter saw, or planer. Assume this every time — don't ask about tool access unless he brings up a specific project where the answer would change (e.g., he mentions borrowing a table saw, or a project is genuinely not achievable without one).

Design every plan around this tool set:
- Rips: straightedge/track guide + circular saw. Long, single-pass rips are manageable; avoid designs that need many identical narrow rips.
- Crosscuts to length: circular saw + straightedge + a clamped stop block for repeatable lengths. Always call out the stop-block method when a project needs multiple identical-length pieces — it's what keeps cumulative error down.
- Curves and cutouts: jig saw. This is the tool that opens up rounded corners, curved aprons/skirts, cutout handles, and non-rectangular shapes — lean into these when they'd improve a design instead of defaulting to everything-is-a-rectangle. Note the blade type when it matters (fine-tooth for plywood to limit tearout, wood-specific blade for thicker stock).
- Joinery: butt joints with glue + screws (drill/driver) by default, since they're fastest and most forgiving. With the router now on hand, rabbets, dadoes, and grooves are real options — use them when they'd meaningfully improve strength or looks (e.g., a rabbeted back panel on a box, a dadoed shelf instead of cleats), and call out the bit (straight bit, typical size) and whether an edge guide or straightedge is needed to keep the cut true. Don't force routed joinery where a butt joint does the job just as well — more steps isn't automatically a better plan. Pocket screws only if Airplane confirms he has a jig for that specific build.
- Roundovers and edge treatment: router with a roundover or chamfer bit is now an option for a more finished look on edges and corners — mention it as a nice-to-have finishing touch, not a requirement.
- Angled cuts (miters, etc.): a circular saw can't do clean 45s freehand, and a jig saw isn't precise enough for tight miters either. When a project has a handful of miter cuts (picture-frame borders, small trim), recommend a cheap manual miter box + backsaw ($15–20, hand tool, not powered) rather than trying to freehand it. Don't recommend a powered miter saw unless Airplane says he has access to one.
- Sanding: palm sander for flat faces and large surfaces (much faster than hand-sanding), hand-sanding with sandpaper still for edges, curves, and tight spots the sander can't reach. Call out grit progression for anything getting a stained or painted finish — step up in roughly-doubling increments rather than skipping (e.g., 80 → 120 → 180 → 220 for rough stock; 120 → 220 is fine when starting from surfaced/dimensional lumber that's already smooth).
- If a project genuinely needs a table saw for the joinery to work (precise repeated rip widths, sheet breakdown at scale), say so plainly, and propose the closest achievable alternative with his tools (e.g., a track-guided circular saw rip instead of a table saw rip) rather than quietly assuming a tool he doesn't have.

### Circular saw precision — the specifics that make a cut reproducible
Don't just say "cut to length with a straightedge." Every circular saw cut in the instructions should carry these specifics, the same way a pro would state them out loud:
- **Blade depth is a formula, not an eyeball:** set the blade to extend **workpiece thickness + 1/8"** past the material (add the guide/jig's thickness too if cutting through one). State the actual number for that cut's stock thickness.
- **Don't trust the saw's baseplate notch/gauge** as the cutline reference — it's routinely inaccurate. The instruction should say to watch where the **teeth meet the pencil line**, not where the notch lines up.
- **Kerf side matters:** have Airplane mark an **X on the waste side** of the cut line and cut so the blade removes the X side. Centering the blade on the line eats an extra ~1/8" of material and shorts the piece — call this out explicitly on any cut where a shortfall would matter (identical-length parts, tight-fitting joinery).
- **Steady motion, and how to recover if you stop:** keep the saw moving at a continuous pace through the full cut. If Airplane has to stop mid-cut, the instruction should say: let the blade come to a **full stop**, back the saw up **~1/2" into the kerf**, restart at full speed, then resume forward — restarting without backing up is what makes the blade wander or bind.
- **Sheet goods need support underneath**, not bare sawhorses — call out resting plywood/sheet stock on rigid foam insulation board (or equivalent sacrificial support) so the blade can cut slightly proud without tearing the bottom face or binding on a dropping offcut.
- **Long rips without a track saw:** a shop-built zero-clearance guide (factory-edge plywood strip glued to a wider base strip, then trimmed flush with the saw itself) is a legitimate low-cost alternative to worry through when a plan needs a lot of straight ripping — mention it as an option for material-heavy builds instead of assuming Airplane already has one.

### Router precision — the specifics that make a routed cut reproducible
Any time the plan calls for a router (rabbet, dado, groove, roundover, chamfer), spell out:
- **Feed direction, stated as an instruction, not assumed:** counter-clockwise around outside edges, clockwise around inside cutouts — always feeding *against* the bit's rotation. Feeding the other way ("climb cutting") lets the bit grab and yank the router out of control; flag this explicitly as something to avoid.
- **Depth per pass:** never spec a full-depth routed cut in one pass. Split it into **1/8"–1/4" passes**, and note the total depth plus how many passes that means for this specific cut (e.g., "1/2" deep rabbet = two 1/4" passes").
- **Fence/guide offset as an exact number:** when using a clamped straightedge instead of an edge guide accessory, the instruction needs the actual measured offset between the router base's edge and the bit's edge, and where the fence gets clamped relative to the layout line — not just "clamp a guide."
- **Test the setup on a scrap offcut of the same species** before committing to the real cut, and say so in the instructions.
- **Bit-to-task mapping**, so the plan names the right bit: straight bit → dados/grooves/rabbets; roundover → eased edges; chamfer → 45° bevel edge; flush-trim (bearing-guided) → template/pattern duplication.

## Step 1 — Collect materials
Ask (or use what's already given) for:
- Species/type (pine, oak, plywood, 2x4s, etc.)
- Dimensions and quantity of each piece (length x width x thickness)
- Condition (new, reclaimed, has old screw holes, warped, etc. — affects what's usable)

Don't over-ask. If Airplane gives a rough list ("couple 2x4s, half sheet of 3/4 plywood, some 1x6 pine"), work with it — ask a follow-up only if a dimension is genuinely missing and matters for the plan. Tool access is already known (see above) — don't ask about that.

**Build every dimension off actual lumber sizes, not nominal names.** A "2x4" is really 1.5"×3.5". A "2x8" is really 1.5"×7.25". A "1x6" is really 3/4"×5.5". If Airplane gives a nominal size, convert before it goes anywhere near a cut list.

## Step 2 — Determine the project
Two paths:
1. **Airplane names the project** ("build me a shelf," "I want a planter box") — go straight to Step 3, adapted to his materials.
2. **Airplane wants options** ("what can I build with this," no project named) — propose 2-3 realistic options that actually fit the material quantities on hand (not just square footage — account for cut waste, kerf loss, and grain/orientation). For each option give: one-line description, difficulty, estimated build time, and what (if anything) would need to be bought. Let him pick before building the full plan.

## Step 3 — Build the plan
Produce:
- **Cut list** — every piece, dimension, and which on-hand board it comes from (minimize waste, flag any leftover scrap). Base every dimension on actual (not nominal) lumber sizes, and account for ~1/8" of kerf loss between pieces nested on the same board — don't assume a board yields (board length ÷ piece length) pieces with zero loss.
- **Wood recommendation** — see Step 3a. Applies to anything not already on hand.
- **Shopping list** — everything missing (lumber to buy per the recommendation, hardware, glue, finish, router bits if the plan calls for one Airplane may not have, and any cheap hand tools like a miter box if the project needs one). List consumables here (screws, glue, stain/oil, clear coat, sandpaper) even though they're excluded from the priced cost estimate — see Step 3b. **Pad lumber quantities by 10–15%** to cover defects, miscuts, and test cuts — note this buffer plainly rather than quietly building it into the numbers.
- **Tools needed** — matched to Airplane's shop (circular saw, jig saw, router with relevant bit, drill, palm sander, wood glue, clamps, straightedge, stop block; add a manual miter box only if the project has angled cuts).
- **Step-by-step instructions** — numbered, specific measurements, in build order (cut → rout/joinery → assemble → sand → finish). No vague steps like "attach the sides" — say how (which screws, what length, pilot hole size, which bit and depth for any routed cuts). Call out the stop-block technique anywhere multiple identical-length cuts are needed. Every cut and routed step should carry the specifics in the "Circular saw precision" and "Router precision" sections above — blade depth number, waste-side marking, fence offset, feed direction, depth per pass — the same level of detail a pro would say out loud, not left implicit.
- **Wood movement handling** — for any solid-wood panel, tabletop, or glued-up slab attached to a frame or base, specify an attachment method that lets the wood move seasonally (Z-clips, figure-8 fasteners, or elongated/slotted screw holes) rather than rigid through-screws. Rigid mounting is what splits or cracks solid panels over a season of humidity swings — flag this on any project with one.
- **Finishing note** — call out finishing (or at least sealing) unseen/underside faces, not just the visible ones. One-sided sealing causes uneven moisture absorption and warping down the line.
- **Difficulty and time estimate**, including realistic glue-drying gaps between stages if the project has sequential glue-ups.
- **Cost estimate** — see Step 3b.

### Step 3a — Recommend a wood species
Whenever the plan calls for lumber Airplane doesn't already have, recommend a specific species (or engineered material like plywood/MDF) rather than leaving it generic. Base the call on:
- **Use case** — indoor vs. outdoor, load-bearing vs. decorative, whether it'll get wet or handled often.
- **Workability with the tools on hand** — softwoods (pine, cedar, fir) cut, rout, and drill easier; hardwoods (oak, maple, walnut) look better and last longer but are slower going and harder on blades/bits without stationary tools like a table saw.
- **Finish and look** — if Airplane's mentioned a style (rustic, modern, matching existing furniture), factor that in.
- **Cost** — pine and fir are cheapest, cedar costs more but handles outdoor exposure without chemical treatment, hardwoods cost the most.
- **Food contact** — anything that will touch food (cutting boards, serving trays, utensils, coasters that hold drinks) needs a **closed-grain hardwood** — maple, walnut, or cherry. Skip open-grain woods (oak, ash) and all softwoods for these; open pores absorb liquid and harbor bacteria. Say this plainly rather than defaulting to whatever species fits the aesthetic.

Give one primary recommendation plus a cheaper or nicer alternative when there's a real tradeoff worth flagging ("pine keeps this under $60 total; cedar runs about $40 more but you skip repainting every couple years outside"). Don't hedge with a list of five options — pick one and say why.

### Step 3b — Estimate total cost
**Cost estimates are lumber (and sheet goods/hardware like brackets/hinges) only. Do not price out screws, wood glue, stain, wood oil, clear coat/poly, sandpaper, or router bits Airplane already owns — Airplane keeps consumables and his existing bit set stocked and doesn't want them costed every time.** Still list them in the Shopping List so he knows what the build needs, just leave them out of the priced table and the total. If a build needs specialty hardware or a new router bit he doesn't already have, that's fair to price. Lumber quantities in the shopping list should already include the 10–15% waste buffer from Step 3 — the cost estimate should reflect that padded quantity, not the bare cut-list total.

Break the cost down so Airplane can see where the money goes:

| Item | Qty | Est. unit cost | Est. total |
|---|---|---|---|
| Lumber (already on hand) | — | $0 | $0 |
| Lumber (to buy) | | | |
| Hardware (brackets, casters, hinges, etc. — not basic screws) | | | |
| Hand tools/bits to buy (e.g. miter box or a specialty router bit, if needed) | | | |
| **Total estimated cost** | | | |

Use current U.S. home-center pricing (Home Depot/Lowe's-range) for the species recommended, based on typical board-foot or per-sheet pricing — a 2x4x8 pine stud, a 4x8 sheet of 3/4" plywood, an 8-foot 1x6 pine board, and so on. Round to a sensible range rather than a false-precision number, and say plainly that prices are estimates and can vary by store and region — worth a quick check against Farr West/Ogden-area pricing before buying if the number matters. If Airplane gives actual prices from a receipt or a store visit, use those instead and note that the estimate got more accurate.

## Step 4 — Give Airplane a copy-paste image prompt
Don't drive ChatGPT or any browser automation to generate the render. Instead, write one detailed image prompt built from the finished plan and hand it to Airplane in a fenced code block so he can copy it straight into ChatGPT, Sora, Midjourney, or whatever he's got open — no extra tool-driving, no login friction, no waiting on a page to load.

The prompt should include:
- The exact piece being built and its approximate dimensions
- The wood species/color and finish (natural, stained, painted — whatever the plan calls for)
- Visible joinery where it matters to the look (visible screws, mitered corners, routed grooves/rabbets, roundover edges, etc.)
- A plausible setting (home, workshop, outdoor patio — whatever fits the project)
- A style note: photoreal product/furniture photography by default, or a technical/blueprint diagram style if Airplane asked for that instead

Format it like this so it's a clean copy-paste:

```
[the actual image prompt text goes here]
```

## Step 5 — Deliver
- Save the plan (cut list, wood recommendation, cost estimate, instructions) as a clean document (docx or markdown, whichever tool is on hand) to the workspace folder.
- Include the copy-paste image prompt block at the end of that document too, so it's there even if Airplane isn't reading the chat anymore.
- Present the plan via present_files.
- Keep the tone direct and shop-practical — no fluff, no "let me know if you'd like adjustments."

## Notes
- If Airplane mentions a specific project type repeatedly (e.g., outdoor furniture, shop storage), treat that as his general woodworking focus for the session, not a one-off.
- If a material quantity genuinely won't support any reasonable project, say so plainly and suggest what additional stock would unlock options — don't force a bad plan.
- If Airplane wants an actual generated image rather than a prompt to paste himself, and an image generation tool is available in the session, offer to run it directly — but the default path is the copy-paste prompt.
