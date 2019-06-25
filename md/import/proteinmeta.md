## Importing Protein Metadata from a CSV File ##

This feature presents a dialog with just two options - firstly, to load a CSV file to import metadata onto existing proteins, and secondly, a display of the format of CSV file the dialog expects in the first case.

The first option will allow the user to select a file and load it, and the dialog will then report on the success of merging the CSV file with the existing proteins: how many proteins have been affected and have many columns (attributes) of metadata were loaded for them. 

The expected CSV format is revealed in the "Expected CSV format" accordion. Basically, the CSV parser here is looking for a ProteinID column containing the SwissProt format (sp|Accession|Name) as a descriptor. Every other column in the CSV file is regarded as metadata and are parsed and added as new or overwriting metadata attributes (name taken from the header row) to the relevant proteins. Each column is expected to be either numeric in value or a hexadecimal colour format. The column "Name" is treated as a special case and will change the displayed name of the protein. 

A simple example of such a CSV file is given here:

    ProteinID,Name,Quantification
    Sp|P02768-A|ALBU_HUMAN,A Human protein,423

Here, Name and Quantification are metadata columns. Quantification is numeric and Name is a special case that replaces the current protein name.