# pyGSEA
A python wrapper for GSEA
## Requirements ##
* Python 3+
* A gene set (.gmt) file from msigdb (or a custom gmt file as long as the format is consistent)
* A data matrix output from the rsem-generate-data-matrix command (custom file is ok)

## Dependencies ##
* Pandas
## Installation ##
```
git clone https://github.com/nungerleider/pyGSEA.git
cd pyGSEA
```
## Usage ##
```
./rungsea [-h] [-t] [-g1] [-g2] -c  -dm  -x GMT -j JAR
optional arguments:
  -h, --help            show this help message and exit
  -t , --title          The text you want as your GSEA plot title
  -g1 , --group1_name   The name of your group 1 samples (i.e. 'Control')
  -g2 , --group2_name   The name of your group 2 samples (i.e. 'Treated')
  -c , --column_separator 
                        The column number of your data.matrix file where the
                        groups switch. For example, entering "4" would imply
                        columns 1-3 are samples from Group 1 and columns 4+
                        are samples from Group 2. Do not count the column with
                        Gene names (which should be column 0 in this case.)
  -dm , --data_matrix   Path to data.matrix output file of the "rsem-generate-
                        data-matrix" command.
  -x GMT, --gmt GMT     Path to the "gmt" file from the msigdb.
  -j JAR, --jar JAR     Path to the "gsea.jar" file.
```
