## Filter Bar ##

![Filter Bar](../../img/filterBarABC.png)

At the bottom of the xiView results visualisation page are a bar of controls for filtering the data. Working from left to right, these fall into the following subsections:

- Modal
- Cross-link attributes
- Then either both of
	- Pass / Fail Threshold (or ABC / Auto / Unval)
	- Score Cut-Off
- Or
	- FDR
- Match Attributes

A summary line at the very bottom of the window describes the effect of the current filtering state on the cross-link data set, and a button is also available to reset the filter state.

### Modal ###

This sub-bar, comprised of two radio buttons: 'Manual' and 'FDR', only appears if unvalidated cross-links have been loaded as well. 'Manual' is selected by default and means the following other sub-bars are available in the filter bar: 'Cross-link positional categories', 'Score Cut-off' and 'Match attributes'. Selecting 'FDR' replaces the 'Cross-link positional categories' and 'Score Cut-off' sub-bars with the FDR sub-bar; the 'Match attributes' sub-bar remains in place.


### Cross-link positional categories ###

These controls allow including or excluding categories of cross-links which are defined on the basis of link position. These categories are:
- Ambiguous - include/exclude cross-links which have an uncertain position due to peptide-level ambiguity (i.e. ambiguity as in the protein identification problem)
- Between - include/exclude cross-links that are between different protein
- Self - include/exclude cross-links between instances of the same protein; note - these cross-links are not necessarily intra-molecular and we avoid using the word 'intra' in this context.
- Homomultimeric Links - a sub-class of Self links in which one of the constituent matches purports to link two overlapping peptides - which is generally not possible.
- AA apart - excludes Self Links with fewer than the specified number of amino acids separating them in the sequence.
- Pep. length - Peptide length. Excludes constituent matches of cross-links where one of the linked peptides is smaller than the set value.

### Pass / Fail Threshold - XiView Public ###

Radio buttons that allow all matches, only those where the 'pass threshold' attribute (as read from the uploaded data) is true, or only those where it is false. This section appears in the Public version of XiView.

### ABC / Auto / Unval - XiView Lab ###

A set of checkboxes that pass or filter out cross-links based on their manually assessed quality (A, B, C and ?), or their algorithmically assessed quality (AUTO), or their validation status (Unval. = unvalidated). This section only appears in the Rappsilber Lab version of the interface as it depends on specialised output from XiSearch.

### Score Cut-off ###

This sub-section allows upper and/or lower score cut-offs for the matches to be set. These is done by entering text in the input fields or dragging on the histogram to set and move a range slider.

Note that the contents of the score histogram shown here is not affected by other filter settings; to see a histogram of scores post-filtering open the [Histogram View](./views/histogram.html "Histogram View").

### FDR ###

When the FDR mode is selected, this sub-bar allows a basic link-level FDR threshold to be set. Matches that do not pass the threshold are filtered out. Five pre-set levels are provided (1, 5, 10, 20, and 50%) along with an open-entry input for other values. FDRs are reported separately for within and between protein cross-link sets.

![Filter Bar FDR](../../img/filterBarFDR.png)

### Match Attributes ###

A number of text boxes that allow matches to be filtered based on the contents of some of their attributes.

'Peptide' filters to matches that include the entered text string as part of one of the peptide sequences it connects.

'Protein' takes in a comma separated list of values that are text matched against protein descriptions and names. Matches that don't link such proteins are filtered out. A hyphen can be used to specify matches that link two particular proteins or sets of proteins. E.g., "ALBU" would show matches that involve a protein containing the text 'ALBU' in its name or description such as ALBU-HUMAN. "BOVINE-CHICK" would show all matches that connect proteins where one protein contains 'BOVINE' and the other 'CHICK'. "ALBU, BOVINE-CHICK" would additively combine the previous two scenarios.

'Charge' filters out matches that do not have the given input charge state, which is always a positive integer. 

'Run' filters out matches whose 'Run' attribute does not contain the entered text as a sub-string.

'Scan' similarly filters out matches whose 'Scan' attribute does not contain the entered text as a sub-string. Whilst 'Scan' is actually a number, treating it as a string here allows more flexibility - entering say '21' will pass all matches whose scan number includes '21' at some position, rather than exactly matching '21'.

'Residue Pairs per PPI' sets a threshold on the number of distinct matches between pairs of proteins that needs to be met before those matches are shown. This can be useful for quickly filtering out weakly interacting protein-protein pairs, and can tidy up the XiNet view in particular.

### Summary ###

In the bottom left of the screen is summary information on the number of cross-links that passed the filter. If decoys were included in the uploaded data then totals will be provided for the number of target-target, target-decoy, and decoy-decoy cross-links passing the filter. For info, an 'apparent link-level FDR' is displayed based on these totals if the FDR mode and value has not been explicitly set.

### Reset Button ###

Finally, in the leftmost position of the filter bar is a button marked 'Reset'. Double-click this button to reset the filter to its initial state. If the search was loaded with a URL that included preset filter values it will reset back to these values.