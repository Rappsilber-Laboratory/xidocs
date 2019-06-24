## Import Cross-Links from a CSV file ##

The CSV File Chooser dialog will ask for up to two files that are needed to load additional cross-links into Xi View. The first file, of CSV format, requires data under fixed column names (though the columns themselves don't need to be fixed in order).

Compulsory columns are:

- Protein1 - The name/ID of the protein at the start of the cross-link
- SeqPos1 or LinkPos1 or AbsPos1 or fromSite - The position in the protein sequence of the start of the cross-link
- Protein2 - The name/ID of the protein at the end of the cross-link
- SeqPos2 or LinkPos2 or AbsPos2 or ToSite - The position in the protein sequence of the end of the cross-link

Other columns such as RunName, ScanNumber, Charge, CalcMass, PepSeq1, PepSeq2 and Score can be added for more information on each cross-link


If Protein1 and Protein2 contain Uniprot accession IDs either as a whole or as a part (typically the 2nd part in a string divided by '|' characters) then sequences can be gathered from Uniprot. Otherwise a second file, a FASTA file, has to be selected too, with the FASTA ids matching the Protein1 and 2 fields in the CSV file.


Example CSV File format:

    Score	Protein1	Protein2	LinkPos1	LinkPos2
    13.06935036	sp|P08518|Rpb2	sp|P08518|Rpb2	218	228
    12.79883956	sp|P08518|Rpb2	sp|P08518|Rpb2	218	228
    12.57750425	sp|P08518|Rpb2	sp|P08518|Rpb2	228	507
    12.34875984	sp|P08518|Rpb2	sp|P08518|Rpb2	228	507
    11.88071586	sp|P08518|Rpb2	sp|P08518|Rpb2	228	507
    11.66168069	sp|P08518|Rpb2	sp|P08518|Rpb2	228	507
    11.52868266	sp|P08518|Rpb2	sp|P08518|Rpb2	228	507
    10.49032147	sp|P08518|Rpb2	sp|P08518|Rpb2	228	507
    10.31234759	sp|P08518|Rpb2	sp|P08518|Rpb2	228	507
    9.145134029	sp|P08518|Rpb2	sp|P08518|Rpb2	228	507
    8.561262414	sp|P08518|Rpb2	sp|P08518|Rpb2	228	507
    8.156446216	sp|P08518|Rpb2	sp|P08518|Rpb2	228	507
    12.06253108	sp|P08518|Rpb2	sp|P08518|Rpb2	987	1102
