# NanoImprint

An R markdown script for creating the output of NanoImprint. A tool for interpretation and visualization of DNA methylation at regions implicated in known imprinting disorders.

## Usage
For reference genome T2T-CHM13v2.0: Download `NanoImprint.Rmd` and `ctrls_2.xlsx`
For reference genome hg38: Download  `NanoImprint_Hg38.Rmd` and `ctrls_hg38.xlsx`
Place the files in your data folder and open the NanoImprint script. Import your data BED files into the `#import data` section and run the script to produce an NanoImprint report. See output examples below.

Data requirements:
* Data should be obtained from modbam2bed included in the [Human variation workflow](https://github.com/epi2me-labs/wf-human-variation) provided by ONTs epi2me labs. Both phased and unphasedBED files is required and should be created using the command line options `--phase_methyl` and `--methyl` in the [Human variation workflow](https://github.com/epi2me-labs/wf-human-variation).
* All three BED files must be sorted with BEDTools intersected before use. Sorting to the  regions can be done using the `region_T2T.bed` or `regions_hg38`file:
`bedtools intersect -a yourfile.methyl.cpg.acc.bed -b regions_T2T.bed > yourfile.methyl.filtered.bed`

### Report output examples:
![Alt text](https://github.com/carolinehey/NanoImprint/blob/main/SRS_plot.PNG)
![Alt text](https://github.com/carolinehey/NanoImprint/blob/main/table.PNG)
![Alt text](https://github.com/carolinehey/NanoImprint/blob/main/all_plots.PNG)
