
```
# Kojak version 1.0 parameter file
# Please see online documentation at: 
# https://code.google.com/p/kojak-ms/wiki/Parameters

# All parameters are separated from their values by an equals sign ('=')
# Anything after a '#' will be ignored for the remainder of the line.

# Data input files: include full path if not in current working directory
database		=	target-and-reverse.fasta
MS_data_file		=	Data1.mzML
output_file		=	Data1.txt
percolator_file		=	Data1-percolator.txt
percolator_version	=	2.04 

# Parameters used to described the data being input to PepLynx
enrichment	=	0	#Values between 0 and 1 to describe 18O APE. For example, 0.25 equals 25 APE.
instrument	=	0	#Values are: 0=Orbitrap, 1=FTICR
MS1_centroid	=	0	#0=no, 1=yes
MS2_centroid	=	0	#0=no, 1=yes
MS1_resolution	=	50000	#Resolution at 400 m/z
MS2_resolution	=	25000	#Resolution at 400 m/z

# Cross-link and mono-link masses allowed. May have more than one of each parameter.
cross_link_mass	=	138.0680742
mono_link_mass	=	155.0946
mono_link_mass	=	156.0786

# Fixed modifications.
fixed_modification	=	C	57.02146

# Differential modifications. @ = N-terminus
max_mods_per_peptide    =       2
modification            =       K       14.015894
modification            =       K       28.031788
modification            =       K       42.047682
modification            =       M       15.9949
modification            =       @       42.01055

# Parameters used in PepLynx analysis
decoy_filter        	=	reverse #identifier for all decoys in the database. Default value is "random" (without quotes)
max_miscleavages	=	4	#number of missed trypsin cleavages allowed
max_peptide_mass	=	10000.0	#largest allowed peptide mass in Daltons
min_peptide_mass	=	550.0	#lowest allowed peptide mass in Daltons
max_spectrum_peaks	=	500	#top N peaks to use during analysis. 0 uses all peaks.
ppm_tolerance_pre	=	15.0	#mass tolerance on precursor when searching
ppm_tolerance_frag	=	10.0	#mass tolerance when scoring fragment ions
prefer_precursor_pred	=	1	#prefer precursor mono mass predicted by instrument software.
search_dimers		=	0       #0=no, 1=yes
relaxed_analysis	=	1       #0=no, 1=yes
top_count		=	500	#number of top scoring single peptides to combine in relaxed analysis
spectrum_processing	=	1	#0=no, 1=yes
use_comet_xcorr		=	1	#0=no, 1=yes

```