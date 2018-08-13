## Xi Legend View ##

![Legend View](../../img/legend.png "Xi Legend View")

This view shows both a table of representation styles used in the various xi views, and controls for changing and setting the active colour scheme used across the views.

The bottom half of the display is taken up with three expandable segments, each of which can be expanded / contracted using the white triangle arrows to the left of each heading.

The bottom two sections, "Protein-Protein Level" and "Residue Level" contain legends for the representation of two different scales of cross-link aggregation - the first for showing aggregated cross-links between  and within proteins, and the second for showing individual cross-links. The main points are that ambiguous cross-links are shown as dotted lines, and aggregated cross-link representations have a grey background whose width is proportional to the number of cross-links within the aggregation.

The first section, "Current Cross-Link Colour Scheme" contains details of the colour scheme currently used across the views. The colours under the "Mark" column are interactive - pressing one will allow the selection of a bespoke colour for that category.

### Options ###

The topmost button, "Download Current Colour Scheme as SVG", downloads a small table of colours and categories in a vector format (SVG) that can be used to complement previously downloaded figures - as long as they use the same colour scheme.

The dropdown "Change Cross-Link Colour Scheme" is used to change the current colour scheme, of which there are four defaults:

1. Cross-Link Type - colour links by between, self or homomultimeric status
2. Protein-Protein Colouring - for small collections of proteins (up to 5) this will generate a unique colour for each possible protein-protein combination a between cross-link could have.
3. Group - for aggregated searches, each cross-link will be assigned a group colour if it is unique to that search group, otherwise, if it is common to searches in more than one group, given a default "Multiple Group" colour. 
4. Distance - when a PDB file is loaded, this colour scheme can be used to discriminate 'within distance', 'borderline' or 'overlong' cross-links. A range slider is also available in this scale to change the cutoff values.

Other colour schemes become available when loading cross-link metadata. Each non-positional column in a cross-link metadata file will be converted to a colour scheme if possible, most usually to a scale between the minimum and maximum values in the column.

Lastly, like the other views that sit in sub-panels, this view can be resized by clicking on and dragging its corners, and repositioned by clicking on and dragging the title bar. The view can be closed using the X button next to the top right-hand corner.




