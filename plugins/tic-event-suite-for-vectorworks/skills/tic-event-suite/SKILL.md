---
name: tic-event-suite
description: Use whenever the user wants Claude to work in their Vectorworks drawing through the TIC Event Suite - draw or change a site plan, place fences, gates, tents, amenities, generators, food trucks, crowd queues, cable ramps or markers, set layers, sheets, viewports or the scale, run Generate Reports, Create Grid Sheet, Update Sheets, Refresh Suite Data or the Event Brief, or lay out an event site.
---

# TIC Event Suite for Vectorworks

The TIC Event Suite connector works on the drawing in front in the user's own Vectorworks, through the TIC-ES Control Panel. Everything Claude does there is one Undo step for the user.

## Before the first call
1. If a reply says no Control Panel is linked, tell the user: open Vectorworks, open TIC-ES Control Panel from the TIC Event Suite menu, and switch Claude link on. Stop until they have.
2. Call an area's `list` action before using it in a conversation. Use the input names it returns, exactly.
3. Lengths and positions are always metres from the drawing's origin, x east, y north, whatever units the drawing shows.
4. Send one call at a time and wait for its answer. Two at once can leave the second unrun.
5. The first time in a conversation, tell the user that what Claude reads from their drawing, pictures included, passes through TIC's connector to Claude.
6. Before a big change, ask the user to save the drawing. Tell them to check every result: Claude can get things wrong.

## Which tool for what
Read `references/tools.md` for every area and when to use it. In short: `read_drawing` and `look` to see; `draw` and `edit_shapes` for plain shapes; `place` for TIC objects; the change tools for their settings; `drawing_settings` for units, scale and georeference; `organise` for layers, classes, sheets and viewports; `suite_jobs` for the TIC menu commands; `event_calculator` for planning figures; `read_manual` for how any TIC tool or report works.

## Rules that keep the drawing safe
- Read before changing. Look at the drawing after any layout change and say what you see.
- A reply starting "Not changed" means nothing happened. Tell the user why in plain words, fix the input, and try once more at most.
- Place TIC objects with `place`, never by drawing their outline.
- Before anything that writes a file (reports, the Event Brief), say what file and where, and wait for a yes.
- Before changing a Vectorworks preference, say it reaches every drawing and cannot be undone, and wait for a yes.
- Never write or run a script in Vectorworks. If no tool does what the user wants, say so.
- Before deleting anything, say what and wait for a yes.
- Before changing more than one object at once, say how many and what, and wait for a yes.
- If the user says to stop asking, stop asking for the rest of the conversation, bar Vectorworks preferences and deletes, which still need a yes.
- Never delete more than the user named.
- Never open or use the TIC-ES AI Helper panel, by any route. Do the work with the connector's tools; the event calculator runs inside the connector.
- Never choose a coordinate system. Offer the ones used at that place with their codes and let the user pick.

## Starting a new site
Read `references/workflows.md`. Ask the scale, whether the drawing is georeferenced (and to what system), and whether it needs a grid, before drawing anything.

## Laying out an event
Read `references/layout.md` before proposing a layout. Take figures from the `event_calculator` tool, or from guidance the user names. Never invent a figure. Every figure is planning guidance only: say so, and that it must be checked with a relevant professional for their own event. Say the calculator's figures draw on UK guidance, the Purple Guide and the Green Guide, and that local rules and the local authority's conditions come first.

## How to talk to the user
Plain words, the ones drafters use: layer, class, sheet, viewport, symbol, record, worksheet, bump in, bump out. Name objects by what they are and their name on the plan. Keep replies short. Never describe how the suite works inside: say what it does for the user.
