## 3D (NGL) View ##

![3D View](../../img/3d.png)

This view integrates the NGL 3D viewer (see references below) within Xi, showing the currently filtered cross-links in the context of a chosen PDB structure.

Positional manipulation of the view is performed by clicking anywhere on the view and dragging the mouse pointer with the following effects:
* Left-click and drag - rotates structure around XY axes (up/down drags around X axis, left/right around Y axis)
* Right-click, CTRL key and drag - rotates structure around Z axis
* Right-click and drag - pans structure in XY plane
* Left-click, CTRL key and drag - pans structure in XY plane (same as above)
* Left-click, SHIFT key and drag - zooms in/out of structure
* Mouse-wheel - zooms in/out of structure (same as above)
* Mouse-wheel and SHIFT key - moves the near clip and far fog effects in and out of the z-axis. Useful for seeing slices of structure but beware doing it by accident. If you're seeing large parts of the structure cut off when you rotate it this is what you've done.

Pressing certain keys also performs operations on the view:
* 'R' - Re-position the structure so it sits in the centre of the window
* 'I' - Slowly rotates the structure around the Y-axis - toggle back off by pressing 'I' again
* 'K' - Slowly oscillate the structure around the Y-axis - aids depth perception of structure

A more in-depth manual for NGL is available here --> [NGL Manual](http://nglviewer.org/ngl/api/manual/index.html "http://nglviewer.org/ngl/api/manual/index.html")

Like the other views in Xi View, individual cross-links can be highlighted by moving the mouse pointer over them (plus a tooltip supplies details on the particular cross-link). Similarly, cross-links can be selected by using the left mouse button. In conjunction with the CTRL key, multiple cross-links can be selected (by clicking on unselected links) and currently selected cross-links can be unselected.

Clicking with the left mouse button on the background of the view will clear all selections.

At the top of the panel that contains the 3D representation is a short piece of textual information giving the PDB filename and the coverage it has of the proteins in the search. This coverage can range from complete (100%) for single proteins with a fully covering PDB to tiny fractions (1-2%) for large protein complexes.

### Options ###

There are a number of options available that can affect the visual presentation of the cross-links in the 3D view.

The "Re-Centre" button re-centres the structure within the panel (also available by pressing "R".)

There are two single selection drop-downs for styling the protein structure itself. The first, "Draw Proteins", changes the style of the protein representation. The default is "Cartoon" with other styles described here --> [NGL Representation Styles]("http://nglviewer.org/ngl/api/manual/molecular-representations.html"). In practice, they range from atom-level representations like "Point" or "Ball+Stick" to more abstract representations such as "Rope" or "Cartoon".

The second selection dropdown, "Colour Proteins", controls the colouring of the protein representations. They range from the default "Uniform" grey colouring to colour schemes that change on a per-atom or per-residue basis such as "Element" or "Residue Name". Consequently, some colour schemes are only useful in conjunction with given representation styles e.g. the "Element" colour scheme works with "Ball+Stick" but has no effect in the "Cartoon" representation. A full list of NGL colour schemes can be found here --> [NGL Colour Schemes]("http://nglviewer.org/ngl/api/manual/coloring.html").

A third drop-down menu, "Show", holds options for setting various decorations on the protein structure, and some options for controlling how cross-links are superimposed upon the structure.

For cross-links there are two independent options, we can:
1. Show selected cross-links only - this reduces clutter and selected cross-links aren't obscured by unselected cross-links, which is particularly noticeable in 3D.
2. Show shortest possible cross-links only - in PDB structures with multiple copies of a protein, there are multiple places a cross-link could be positioned. E.g. in a dimer structure (protein copies A and B) a cross-link between positions 1 and 2 could have four possible solutions, A1-A2, A1-B2, B1-A2 or B1-B2. This setting, selected by default, tells the view to show only the shortest possible cross-link out of these possibilities.

The other available options under "Show" are
* Show Cross-Linked Residues - represent residues as balls at the ends of displayed cross-links.
* Show All Proteins - show proteins in multiple protein PDBs that aren't potentially involved in the current set of filtered cross-links. 
* Show Distance Labels - displayed cross-links are annotated with a small label showing their length in Angstroms. These show up regardless for selected or highlighted cross-links.
* Protein Chain Label Style - Long, Short, None - a set of radio buttons for deciding the content of the label annotating each protein. Long for a verbose description which NGL pulls from the PDB file (plus the short description), short for a label with the protein name and chain index, and none to remove these labels altogether.

There is one remaining button which sits by itself, "Download Image as PNG", which will download a PNG (bitmap format) file of the current state of the 3D view. A vector graphic format is not available for this view. The filename will include information on search id and current filter settings.

Lastly, like the other views that sit in sub-panels, the 3D view can be resized by clicking on and dragging its corners, and repositioned by clicking on and dragging the title bar. The view can be closed using the X button next to the top right-hand corner.

### References ###

* AS Rose, AR Bradley, Y Valasatava, JM Duarte, A Prlić and PW Rose. _NGL viewer: web-based molecular graphics for large complexes._ Bioinformatics: bty419, 2018. [doi:10.1093/bioinformatics/bty419](http://dx.doi.org/10.1093/bioinformatics/bty419)
* AS Rose and PW Hildebrand. _NGL Viewer: a web application for molecular visualization._ Nucl Acids Res (1 July 2015) 43 (W1): W576-W579 first published online April 29, 2015. [doi:10.1093/nar/gkv402](https://doi.org/10.1093/nar/gkv402)


