## Xi Search History Page ##
The Xi Search History page is a paged table consisting of one row per search, with columns detailing meta-data for each search. Restricted users will see only their own searches; standard users can also see all non-private searches from other users. Superusers (Xi Administrators) can see all searches regardless of the search privacy settings.

### Title Bar ###
For non-restricted users, the title bar contains a radio button option to see either only your searches or all searches you have permission to see - the default is to see only your own searches. Also, dependent on being a non-restricted user, there will be a button to launch a new search i.e. go to the [Search Submit](../../html/searchSubmit/index.html) page. There are also buttons that link to the [User Admin](../../html/userGUI/index.html#userAdmin) page and to log out of Xi.

### Table Controls ###
Paging is controlled through the *Page Number* control at the top left.

Filtering is performed by entering text in the text fields below the table headers. Filters in different columns are applied conjunctively, i.e. a search must satisfy all filters to be shown.

Sorting can be done on columns with an arrow icon next to the filter text field. The default sort is by date.

These controls can be used together to find searches of interest, though generally the filtering is the most useful.

### Visualise a Single Search ###
Links in the first two columns - *Visualise Search* and *+FDR* - launch the [Xi Visualisation](../../html/xi3/index.html). The first column's link only loads auto-validated crosslinks into the visualisation. The second column's link (*+FDR*) also loads decoy and unvalidated crosslinks, which allows basic FDR (False Discovery Rate) calculations to be used as a filter within the visualisation.

### Visualise Aggregated Searches ###
Aggregate multiple searches for visualisation using the text fields in the *Agg Group* column. Enter a number in the text field for each search that should be aggregated. **Number Meaning**:  Searches marked with the same number will be coloured the same in the resulting visualisation - so enter the same number if you want searches to be indistinguishable, and enter different numbers for searches you wish to differentiate visually.

Press the *Aggregate* button in the title bar to view the aggregated searches with auto-validated links only. Press the *Agg. For FDR* button to include decoy and unvalidated links so an FDR filtering can be performed in the visualisation (exactly as for the single search).

### Validate a Search ###
Click the underlined 'Validate' text in the *Validation* column to show a selection dialog for a particular search. This dialog has options to validate various combinations of cross-links - including linear peptides and/or decoy proteins. Selecting an option will then take you to the search's validation page and populate it with the requested links.

### Delete a Search ###
Delete a search by pressing the button in the *Delete* column for a search. If the button is not present, you don't have the rights to delete it. A dialog will then appear asking if you are sure you wish to delete the search - as this cannot be undone unless you are a superuser.

### Other Information ###
Other columns show additional meta-data relating to individual searches.
- *Visualise Search*: The search state is appended to the name of the search in this column. This shows whether a search is queuing, being processed, has an error, or has completed. Uncompleted searches will not have a link to launch the visualisation.
- *Notes*: If a search had notes added when it was submitted in the [Search Submit](../../html/searchSubmit/index.html) page they will be shown here. Generally a tooltip will be needed to see the full text.
- *Sequence*: The file name of the .fasta file used in the search.
- *Enzyme*: The enzyme used in the search.
- *Cross-Linkers*: A list of the cross-linkers used in the search.
- *Submit date*: The date the search was submitted.
- *ID*: Search ID.
- *User*: The user who submitted the search.


