# Common jobs, in order

## A new site plan
1. open_blank_drawing, or confirm the user wants the drawing in front.
2. Ask the scale; drawing_settings scale.
3. Ask whether to georeference. If yes, ask the place and offer the coordinate systems used there; drawing_settings georeference with the user's choice.
4. Ask whether the site needs a grid. If yes, draw or place the main items first, then suite_jobs grid_overlay so the grid covers them.
5. Draw the boundary on its own layer if the user gives one.

## A fence line with gates
1. place a Fence Run along the points.
2. place each Fence Gate on the run at its start point, with its width as length.
3. read_drawing fields on Fence Gate before marking an exit, then change the gate.
4. look to check.

## Tents, amenities, generators, food trucks
1. read_drawing fields on the kind for its settings and choices.
2. place each one with the fields the user gave.
3. If Place says the choices load when the palette shows the object, it is placed and selected: set those fields next with the change tools on the name it gave.

## Reports and counts
1. suite_jobs refresh, scope all.
2. Say which reports and where the files go; wait for a yes.
3. suite_jobs reports with the names, or all, and the outputs asked for.
4. Tell the user what each report said, including why any wrote nothing.

## Grid sheets
1. suite_jobs grid_overlay if there is no grid.
2. suite_jobs create_grid_sheet with paper, orientation, scale and title; the frame box appears.
3. Ask whether to move it; then suite_jobs create_grid_sheet again with nothing.
4. suite_jobs update_sheets after later changes.
5. look at the sheet.

## The Event Brief
suite_jobs event_brief saves a blank brief to Downloads or the folder used last, for the organiser to fill in. Say so first.
