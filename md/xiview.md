## Xi View ##

Xi View contains many different ways to view cross-link data, from circle plots, protein network views, protein sequence views and tables, to raw spectra and peak views. Data can be filtered and exported, as can images. PDB datasets can be incorporated to give physical context to the cross-links, enabling 3D and contact map views, with automatic alignment performed between Xi and PDB sequences.

This documentation is divided into four logical sections:

1. Filtering Data
2. Viewing Data
3. Exporting Data

### 1. Filtering Data ###

One of the main benefits of XiView is the ability to filter the dataset based on various attributes. A description of the full set of the available attributes and operations can be found here on the [Filter Bar](./views/filterBar.html "Filter Bar") page.

### 2. Viewing Data ###
There are a number of different views available for exploring cross-links within Xi View. One, the XiNet view, is a constant in the main window of xiView. The others are available via the "View" drop-down menu in the menu bar along the top of the window.

The views themselves can be categorised as three basic types:

* Those that show positional cross-link data:
	1. [Xi Net](./views/xinet.html "Xi Net")
	2. [Circular View](./views/circular.html "Circular View")
	3. [Matrix View](./views/matrix.html "Matrix View") aka Contact Map
	4. [3D NGL View](./views/3dngl.html "3D View")
	5. [Protein Info View](./views/proteinInfo.html "Protein Info View")

* Those that show cross-link metadata:
	1. [Histogram View](./views/histogram.html "Histogram View")
	2. [Scatterplot View](./views/scatterplot.html "Scatterplot View")

* Those whose main purpose is to act as sanity checks:
	1. [Alignment View](./views/alignment.html "Alignment View")
	2. [Search Summaries](./views/searchSummaries.html "Search Summaries")

The [Legend View](./views/legend.html "Legend View") can be considered in a category of its own, its main function to choose and refine a colour scheme used in the rest of the Xi View interface.

#### Filtering ####
All the positional and metadata views above reflect the current filter state, only showing cross-links / matches that pass the filter settings.

#### Selection ####
All the positional and meta-data views also support the idea of selecting / highlighting specific cross-links and matches, with selections and highlighting performed in one view reflected in other active views.

#### Relation to Viewing Spectra ####
The [Selected Match Table](./views/selectionTable.html "Selected Match Table") acts as the bridge to the underlying raw data displayed in the [Spectrum View](https://spectrumviewer.org/help.php "Spectrum View") - open the xiSpec Feature Support section in this link for spectrum viewer use instructions. Selecting a match in this table will displaying the underlying raw data in the Spectrum View.

### 3. Exporting Data ###

![Export Dialog](../img/export.png)

The Export menu in the top menu bar has a number of options for outputting the current filtered set of cross-links or matches.

The first three offer the export in CSV format of various levels of information - cross-links, matches or residues. The Cross-Links export option will output a CSV containing the Cross-Link ID, position of the ends of the cross-link in terms of protein, peptide start position and position within the peptide. Other columns in the CSV will describe the number of matches, the highest score, and the validation status of the Cross-Link. If a PDB file has been loaded the distance and PDB co-ordinates of the link will be output if the Cross-Link has a valid distance. The shortest non-homomultimeric distance is chosen if multiple distances can be attached to the Cross-Link. Finally, for aggregated searches a column per search is present, indicating if the Cross-Link occurred in that particular search or not.

The Matches export option performs a similar function to matches. Extra columns here include raw peptide sequences, charge, mass (experimental and calculated), mass/charge ratio, mass error, scan numbers and indices, crosslinker mass, fragment tolerance and ion types. Not all of these may be populated - it will depend on whether they are present in the input data. Similarly, distance data is also output if present, with the nuance that ambiguous matches can have multiple distances (the shortest one for each cross-link they could represent), and these are supplied as quoted comma-separated lists (so they won't break the csv format).

The Residues export option outputs a much simpler csv file indicate how many times certain residues (AAs) turn up in the cross-link data set and how often each pairing of residue occurs. This is useful for confirming that cross-links only go between given residues.

All exported CSV files are saved with timestamped file names that include a shorthand of the current data filter state.

The final option "Make Filtered Xi URL" offers the option to export a URL that includes the current filter state. Upon re-opening in a browser this URL will set the filter to the values in the URL as a convenient shortcut.

Finally, almost every view has the option to save their current representation as a SVG file, which again includes a timestamp and filter state within the filename.
