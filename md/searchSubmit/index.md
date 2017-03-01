## Xi Search Submission Page ##

The Xi Search Submission Page is the mechanism through which new searches are specified and passed to Xi. The page is broken into 3 logical steps (and the final Submit action). The sections below describe what each step does and how to complete it.

### 1. Choose Acquisitions ###
Acquisitions may be included in a new search in two ways.
1. Construct a new acquisition to be uploaded to the Xi Database and then used in a search.
2. Choose from a list of previously uploaded acquisitions. Depending on your profile rights, you may see only your own previous acquisitions or those uploaded by other users too.

#### Upload New Acquisition ####
Open the accordion section labelled *Upload New Acquisition*. A small form will appear. Three actions need to be completed before the upload is ready to start.
1. Pick and enter a name for the acquisition you are uploading. Choose something that's descriptive of the data you are going to upload.
2. Press the *Add Files* button to open a file dialog to choose one or more files to be parcelled up into this acquisition. Xi currently supports .mgf, .msm, .apl and .zip files and so you are limited to selecting these types of file. Once you have chosen your files they will be listed below the form.
3. Decide whether you wish this upload to be private to yourself by ticking the *Set Upload To Private* checkbox.

Once steps 1 and 2 have been completed to the form's satisfaction the *Start Upload* button will be enabled. Press this to start the upload. Progress bars will then show the upload completing, and upon completion, the files will be relisted as "Uploaded". A text box will also appear under the *Choose Acquisitions* label to indicate this upload has been automatically added to the current set of chosen acquisitions. The close button in the text box will uninclude it.

#### Choose Previous Acquisitions ####
Open the accordion section labelled *Choose Previous Acquisitions*. This, with restrictions according to your user profile, reveals a paged table of previous acquisition uploads to choose from.

The table is sorted by *Id* by default, which produces an identical ordering to sorting the table by *Date*. The table can also be sorted by other metadata: *Name*, *User*, *Files*, or *#* (File Count); and pages can be navigated using the *Previous ... Next* controls in the bottom-right corner. However, the most useful tool for finding acquisitions is the *Find* input box in the top-right corner. This will accept multiple partial strings to match acquisition metadata against and shrink the table to those that match.

Tick the checkboxes in the *Choose* column to choose one or more acquisitions. Choices made here will be added to the collection of text boxes under the *Choose Acquisitions* label. Untick the checkboxes in the *Choose* column or press the close icons in the textboxes to undo a choice.

### 2. Choose Sequences ###
The *Choose Sequences* step is equivalent to the *Choose Acquisitions* step except for these differences:
1. Only one file can be associated with a new sequence upload.
2. Sequence uploading accepts .fasta or .txt files.
3. The table in *Choose Previous Sequences* lacks a File Count column as the count is necessarily always 1.

### 3. Set Search Parameters ###
This step involves setting the following parameters for the new search:

* Name (optional)
* Cross-Linker
* Enzyme
* Ms Tolerance
* Ms2 Tolerance
* Missed Cleavages
* Fixed Modifications
* Variable Modifications
* Ions
* Losses
* Search Notes (optional)

*Name* is used in the search listings in the [Xi Search History](../history/history.html) page. Choose a name that reflects the search, otherwise it will default to concatenating all the chosen acqusition names along with a timestamp.

*Cross-Linker* and *Enzyme* are single choices and the drop-down menu for both reflects that. Use the radio buttons within each respective drop-down to make your choice.

*Ms Tolerance* and *Ms2 Tolerance* are numeric inputs and also have a choice of units (parts per million or Daltons).

*Missed cleavages* is a numeric input with no units.

*Fixed Modifications*, *Variable Modifications*, *Ions* and *Losses* are all parameters for which multiple choices can be made. Select as many options as the search requires using the checkboxes in each parameters' drop-down menu. *Ions* has the extra restriction that at least one of the options must be chosen.

*Search Notes* can be used to add more information about the search, useful as a memory aid for later. The *Custom Settings* textbox is really only used by the Xi Database Admin to set custom flags to a search, and not intended for general use.

To reduce user input fatigue a set of sensible defaults are displayed, so you only need to change the ones that are unsuitable for your new search. These defaults can be restored using the *Use Default Parameters* button. The parameters from your last search can be reapplied using the *Use Your Last Search Params* button. 

### 4. Submit ###

If the previous steps have been completed, then the *Submit New Search* button will be enabled and the neighbouring warning message will have changed from red to green. If there are still uncompleted parts of the page the warning message will still be red and list the missing information types.

Choose whether you wish the search to be private using the *Set Search As Private?* checkbox. This acts in a similar manner to the private acquisition and sequence upload options, in that a private search will only be visible to you and Xi administrators.

Once happy with the choices made on the page, press *Submit New Search* to register and start the search on the Xi Search Engine. You'll then be directed to the [Xi Search History](../history/history.html) page where its progress can be monitored, or another new search begun.

