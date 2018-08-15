## Alignment View ##

![Alignment View](../../img/alignment.png)

Search sequences in the search data can often be slightly different from the sequences for the same proteins in the Uniprot database, and often radically different to those in PDB files for the same proteins. These differences are usually due to missing end and start sequences but can also include residue differences within the sequence and misalignments. Xi View automatically aligns these different sequences so Uniprot annotations appear in the correct place and cross-links in the 3D view are correctly positioned. This view displays the results of these alignments for user inspection along with some controls for tweaking the alignment algorithm (Gotoh) used.

### Options ###

Proteins are displayed as a set of tabs at the top of the view, with options for sorting the tabs if more than one protein is present. These options being:

* Sort by name
* Sort by number of aligned sequences
* Sort by the total score of aligned sequences

Upon selection of a protein the sequences associated with it are shown in the middle portion of the view. Each uniprot or pdb sequence is paired with the search sequence for that protein and the alignment showed as a pair of strings. Moving the mouse over the string for the Uniprot or PDB sequence will reveal details as to the parts of the sequence which are matching, missing or extra to the search sequence.

Beneath this section is a trio of radio buttons for controlling the display of the strings in the sequence pairs. Either the entire strings can be shown ("show all"), or only the matching portions of the strings ("show similarities only"), or only the different portions of the strings ("show differences only"). Resulting elided sections of the strings are replaced with a sequence of quotation marks, whose length is logarithmically related to the length of the elided section.

At the bottom of the panel are three controls for tweaking the Gotoh alignment algorithm. Both the "Gap Open Penalty" and the "Gap Extend Penalty" quantities can be changed, along with the Blosum matrix type the alignment scoring is derived from. These changes are local to the protein currently under examination in this view.
 
Lastly, like the other views that sit in sub-panels, this view can be resized by clicking on and dragging its corners, and repositioned by clicking on and dragging the title bar. The view can be closed using the X button next to the top right-hand corner.




