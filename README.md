# RSCPUcal
RSCPUcal: Determine Relative Synonymous Codon Pair Usage (RSCPU)
## Description
- RSCPUcal is a python package for the analysis of Relative Synonymous Codon Pair Usage in DNA coding sequences. It implements the RSCPU described by Duy et al.(2016).
- This package is writen by Yucong Xu and Lingming Kong.
- If you have any doubts, questions, bug reports, etc. please contact us at:
- Lingming Kong* (acq613@outlook.com)
- Add: Marine College, Shandong University, Weihai, P.R.China 264201
## Required Third Party Resources and Installation
- openpyxl
## Usage
This Python module is used to process sequence.(File extension name '.txt' is required) You can refer to the test documents.
### Required arguments:
- A list of file names that need to be processed. (Only the main file name is required, and no extension name is required, e.g. name=[‘NC_01703.1’,’NC_01425.1’])
- Please download 'zero.xlsx','RSCPU_template.xlsx' before use.
```Python
   import RSCPU_count
   import RSCPU_formula
   name=[]
   a=RSCPU_count.RSCPU_s(name)
   b=RSCPU_formula.RSCPU_g(name)
```
### Output
The output of the module is a file. The title of each column in the file is the file name in the list, and the value of each column is the corresponding calculation result. (for example, new_RSCPU.xlsx)
## Details
- There are 3,721 coding codon pairs, if using a standard translation table. The equation to compute RSCPU for a pair of codon is as follows:
![formula](https://raw.githubusercontent.com/canacexu/RSCPUcal/main/formula.jpg)
- where xi is the number of the occurrences of the ith kind of codon pairs, and ni is the number of synonymous codon pair for the ith type amino acid pair.
- The input of the function is a list of CDS sequence txt, you can find an example in the folder TEST in the RSCPUcal directory.
## References
Duy NHM, Tuan-Anh T, Viet NQ, et al. Identifying species based on relative codon pair usage combining k-means and svm: An application for bacillus. In: Proceedings of the 10th International Conference on Ubiquitous Information Management and Communication. ACM: 2016. p. 41. 10.1145/2857546.2857588.
## Citation:
Lingming Kong (2021). RSCPUcal: Determine Relative Synonymous Codon Pair Usage (RSCPU).
