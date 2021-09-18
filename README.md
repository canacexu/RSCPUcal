# RSCPUcal
RSCPUcal: Determine Relative Synonymous Codon Pair Usage (RSCPU)
## Description
- RSCPUcal is a python package for the analysis of Relative Synonymous Codon Pair Usage in DNA coding sequences. It implements the RSCPU described by Novoa et al. 2019.
- This package is writen by Yucong Xu and Lingming Kong.
- If you have any doubts, questions, bug reports, etc. please contact us at:
- Lingming Kong* (acq613@outlook.com)
- Add: Marine College, Shandong University, Weihai, P.R.China 264201
## Required Third Party Resources and Installation
- openpyxl
## Usage
This Python module is used to process excel worksheets.(File extension name '.xlsx' is required) You can refer to the test documents.
### Required arguments:
- A list of file names that need to be processed. (Only the main file name is required, and no extension name is required, e.g. list=[‘test_1’,’test_2’])
- Please download 'RSCPU_template.xlsx' before use.
```Python
   import RSCPUcal
   list=[]
   a=RSCPUcal.RSCPU_count(list)
```
### Output
The output of the module is a file. The title of each column in the file is the file name in the list, and the value of each column is the corresponding calculation result. (for example, new_RSCPU.xlsx)
## Details
- There are 3,721 coding codon pairs, if using a standard translation table. The equation to compute RSCPU for a pair of codon is as follows:
![formula](https://raw.githubusercontent.com/canacexu/RSCPUcal/main/formula.jpg)
- where xi is the number of the occurrences of the ith kind of codon pairs, and ni is the number of synonymous codon pair for the ith type amino acid pair.
- The input of the function is a contingency file, you can find an example in the folder XXX in the RSCPUcal directory. You should firstly make the file by software ANACONDA 2.0 (https://bioinformatics.ua.pt/software/anaconda/). 
## References
Novoa, E. M., I. Jungreis, O. Jaillon, and M. Kellis. 2019. Elucidation of Codon Usage Signatures across the Domains of Life. Molecular Biology and Evolution 36:2328–2339.
## Citation:
Lingming Kong (2021). RSCPUcal: Determine Relative Synonymous Codon Pair Usage (RSCPU).
