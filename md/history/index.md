## Xi Search History Page ##
The Xi Search History page is a paged table consisting of one row per search, with columns detailing meta-data for each search. Restricted users will see only their own searches; standard users can also see all non-private searches from other users. Superusers (Xi Administrators) can see all searches regardless of the search privacy settings.

### Title Bar ###
For non-restricted users, the title bar contains a radio button option to see either only your searches or all searches you have permission to see - the default is to see only your own searches. Also, dependent on being a non-restricted user, there will be a button to launch a new search i.e. go to the [Search Submit](../../html/searchSubmit/index.html) page. There are also buttons that a) link to the [User Admin](../../html/userGUI/index.html#userAdmin) page, b) link to this help page, c) allow logging out, and a *Keep* checkbox which is explained at the end of the next section.

### Table Controls ###
Paging is controlled through the *Page Number* control at the top left.

Hiding or showing columns of interest can be done using the "Show Columns" dropdown. Uncheck or check the individual columns according to preference.

Filtering is performed by entering text in the text fields below the table headers. Filters in different columns are applied conjunctively, i.e. a search must satisfy all filters to be shown. An individual filter can contain several terms; again these are applied conjunctively e.g. "lum bs3" in the Visualise Search column will only match searches with both "lum" and "bs3" in their names.

Sorting can be performed on those columns with an arrow icon next to the filter text field. The default sort is by date.

These controls can be used together to find searches of interest, though generally the filtering is the most useful.

The *Keep* control in the title bar, if checked, will keep the current filtering and sorting settings for when the history page is next accessed on the same computer.

### Visualise a Single Search ###
Links in the first two columns - *Visualise Search* and *+FDR* - launch the [Xi Visualisation](../../html/xi3/index.html). The first column's link only loads auto-validated crosslinks into the visualisation. The second column's link (*+FDR*) also loads decoy and unvalidated crosslinks, which allows basic FDR (False Discovery Rate) calculations to be used as a filter within the visualisation.

### Visualise Aggregated Searches ###
Aggregate multiple searches for visualisation using the number input widgets in the *Agg Group* column. Enter a number for each search that should be aggregated. **Number Meaning**:  Searches marked with the same number will be coloured the same in the resulting visualisation - so enter the same number if you want searches to be indistinguishable, and enter different numbers for searches you wish to differentiate visually.

Press the *Aggregate* button in the title bar to view the aggregated searches with auto-validated links only. Press the *Agg. For FDR* button to include decoy and unvalidated links so an FDR filtering can be performed in the visualisation (exactly as for the single search).

### Validate a Search ###
Click the underlined 'Validate' text in the *Validation* column to show a selection dialog for a particular search. This dialog has options to validate various combinations of cross-links - including linear peptides and/or decoy proteins. Selecting an option will then take you to the search's validation page and populate it with the requested cross-links.

### Delete a Search ###
Delete a search by pressing the button in the *Delete* column for a search. If the button is not present, you don't have the rights to delete it. A dialog will then appear asking if you are sure you wish to delete the search - as this cannot be undone unless you are a superuser.

### Restart a Search ###
Restarting a stalled search can be performed by pressing the Restart button that may appear in this column. Completed and active searches will not display this option. Again, the buttons also only appear if you have permission to restart that search, and a dialog will ask if you definitely wish to proceed with this operation.

### Base a New Search on an Existing Search ###
The process of setting up the [Search Submit](../../html/searchSubmit/index.html) page can be eased by pre-populating it with another search's parameters. Show the *Base New* column via "Show Columns" and then select the button in the column for the existing search you wish to base a new search on. Note that parameters does not include the sequence and acquisition files.

### Other Information ###
Other columns show additional meta-data relating to individual searches.

- *Visualise Search*: The search state is appended to the name of the search in this column. This shows whether a search is queuing, being processed, has an error, or has completed. Uncompleted searches will not have a link to launch the visualisation.
- *Notes*: If a search had notes added when it was submitted in the [Search Submit](../../html/searchSubmit/index.html) page they will be shown here. Generally the tooltip will be needed to see the full text - hover over the text to see it.
- *Sequence*: The file name of the .fasta file used in the search.
- *Enzyme*: The enzyme used in the search.
- *Cross-Linkers*: A list of the cross-linkers used in the search.
- *Submit date*: The date the search was submitted.
- *ID*: The search ID.
- *User*: The user who submitted the search.


