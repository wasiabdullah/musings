# Miniconda commands

`conda info` 


`conda update conda`


`conda update --all -y`


`conda info --envs`

`conda info -e`

`conda env list`

`conda list`


`conda env remove --name nameofenv`


`conda create --name envname pyton=x.x.x`


`condalist revisions`


`conda install --revision numberof revision`


`conda install --name envname toolname`


`conda remove --name envname toolname`


`conda list --explicit > name.txt`  save environment to text file

`conda env create --file filename.txt`  create envirionment from textfile


creating dependencies requirements file using miniconda

pip freeze > requirements.txt

###  Difference between creating a virtual environment with a requirements.txt file
### and a environment.yml file?