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

To import a filled brief from Downloads: suite_jobs import_event_brief with file (its name in Downloads, or last for the newest). The first run imports nothing and says what it will lay and replace. Say that to the customer, wait for yes, then run it again with go true. Add site when the brief has more than one site. One Undo takes the import back.

## Import a file into the drawing
suite_jobs import_file with file: its full path on the customer's computer, or its name in Downloads. It imports DXF, DWG, IFC, OBJ, 3DS, IGES, SAT, Parasolid (x_t), SketchUp, PNG, JPG and TIF with no box. Revit, shapefile, PDF and anything else are imported in Vectorworks: File > Import.

A DXF or DWG on a georeferenced drawing lands on its real-world position, its numbers read in the drawing's coordinate system. Say which system that is before importing, as a file drawn in another system lands in the wrong place. A file with no real-world numbers stays where it was drawn.

For an OBJ ask what one unit in the file is and pass units: mm, cm, m, in or ft. For an image pass x, y for its centre.

Check the size first. Run import_file with check true: it imports nothing. For a DXF or OBJ it reads the file's own width and depth; for a SketchUp file it reads the units the file is set to; for any other kind it says the size cannot be read yet. Put what it says to the customer and ask whether it is right for what the file is: a stadium 130 millimetres wide was drawn in the wrong units.

After any import the answer gives the size it came in at. Say it to the customer and ask the same question. A wrong size means the file was drawn at that size: Modify > Scale Objects in Vectorworks puts it right. Edit > Undo does not take an import back.

A file of 5 MB or more answers first with its megabytes and imports nothing. Tell the customer it can take from a few minutes to over half an hour and Vectorworks will not answer until it is done, wait for yes, then run it again with go true.

## The Event Brief from the portal
To take the client's brief straight off the TIC client portal: suite_jobs sync_event_brief. With no event it lists the events this licence can sync; then run it with event. It answers the same way as the import: say what it will change, wait for yes, run again with go true.

## The Drawing Audit and Publish
suite_jobs audit and suite_jobs publish both answer first with words for the customer. Say them word for word, wait for yes, then run again with go true. Publish needs reports run with html true first.
