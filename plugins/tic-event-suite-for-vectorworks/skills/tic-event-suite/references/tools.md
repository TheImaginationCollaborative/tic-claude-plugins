# The areas of the TIC Event Suite connector

Call `list` on an area first. These notes say when to reach for each one.

| Area | Use it to | Notes |
|---|---|---|
| open_blank_drawing | Start a new drawing in metres | No dialog. Then set the scale. |
| read_drawing | Count what is in the drawing, list each object of a kind with its settings, or list the fields a kind carries | Start with `by: drawing`. Use `reading: fields` before changing a setting, for its exact name and choices. |
| look | See a picture of the Vectorworks window or a sheet | If a sheet looks blank straight after a change, look again. |
| draw | Lines, rectangles, squares, circles, ovals, arcs, polylines, polygons, text | Shapes are centred on x, y. Optional class, layer, fill, pen, line weight, rotation. |
| edit_shapes | Move, rotate, mirror, duplicate, duplicate array, align, group, ungroup, delete | Name objects as Draw and Place named them, such as Rectangle 1. Ask before every delete. |
| place | TIC objects and symbols | Point objects at x, y; gates and marker points from x, y with a length; tents centred with width and depth; fences, marker areas, crowd queues and cable ramps along points; title block and key on a sheet layer. Set fields by their palette words. |
| change_one_object, change_many_objects | Change a setting on TIC objects | Name them by label, number, name or the name Place gave; "all" for every one of the kind. Lengths need a unit: 2.4 m. Picks must be one of the choices `read_drawing` lists. |
| drawing_settings | Units, layer scale, origin, georeference, Vectorworks preferences | Preferences reach every drawing and have no Undo. |
| organise | Design and sheet layers, classes, visibility, active layer and class, viewports, saved views | A viewport is placed where the drawing falls on the sheet; tell the user to drag it into place. |
| suite_jobs | Refresh Suite Data, Generate Reports, place the grid overlay, Create Grid Sheet, Update Sheets, Find Grid Location, the blank Event Brief, Import Event Brief, Sync Event Brief, Drawing Audit, Publish, Import a file | Create Grid Sheet runs twice: first it drops a frame box, the user may move it, then run it again with nothing. Reports and the Event Brief write files. Import, sync, audit and publish answer first with what they will do: say it to the customer, wait for yes, run again with go true. Import a file takes its full path or its name in Downloads; a big file answers first with its size, so say the wait and run again with go true. |
| event_calculator | Toilets, water, entries, bars, food, security, first aid, waste, site area and accessibility for a crowd size and event type | Planning guidance only, drawn from UK guidance; say so, and that a relevant professional checks it against local rules for their event. |
| read_manual | How any TIC tool, report or worksheet works | Search by words. Use it rather than guessing. |
