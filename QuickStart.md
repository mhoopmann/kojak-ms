# Navigation #
  * [Return to Table of Contents](TableOfContents.md)
  * [Jump to Parameters](Parameters.md)

# Introduction #

Step-by-step instructions to analyzing your mzXML or mzML data. Detailed instructions can be found on other pages in this wiki (links soon).


---


## Step 1: Set up a data project folder ##

> a. Create a folder or directory on your computer hard drive.
    * _Example: ` C:\Data\MyProject\ `_
> b. Copy or link your data to this directory.
    * _Exmaple: ` C:\Data\MyProject\DataFile1.mzML `_
> c. Create a copy of the [Kojak configuration file](SampleConfigurationFile.md) in this directory.
    * _Example: ` C:\Data\MyProject\Kojak.conf `_

## Step 2: Edit your configuration file ##

> a. Open _Kojak.conf_ in a text editor.

> b. Change _MS\_data\_file_ to your data file.
    * _Example: ` MS_data_file = C:\Data\MyProject\DataFile1.mzML `_
> c. Name your _output\_file_ and _percolator\_file_.
    * _Example: ` output_file = C:\Data\MyProject\DataFile1-results.txt `_
    * _Example: ` percolator_file = C:\Data\MyProject\DataFile1-percolator.txt `_
> d. Change _database_ to the amino acid sequence database you want to use.
    * _Example: ` database = C:\FASTA\MyDatabase.fasta `_
> e. Set other parameters as necessary. Parameters and descriptions can be found on the Parameters page.

> f. Save _Kojak.conf_ and exit the text editor.

## Step 3: Run Kojak ##

> a. Open a command line prompt.
> b. Navigate to the Kojak folder.
    * _Example: ` cd C:\Kojak `_
> c. Execute the Kojak application with the path and name of your configuration file.
    * _Example: ` Kojak.exe C:\Data\MyProject\Kojak.conf `_

## Step 4: Validate and Summarize Results ##

> a. Navigate to your data folder
    * _Example: ` cd C:\Data\MyProject `_
> b. Execute the Percolator application
    * _Example: ` C:\Percolator\Percolator.exe -j DataFile1-percolator.txt > DataFile1-validated.txt `_
> c. View your _` DataFile1-validated.txt `_ results file in any text editor or spreadsheet application (such as Excel).