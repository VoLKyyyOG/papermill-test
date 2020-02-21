# Links
Docs - https://papermill.readthedocs.io/en/latest/usage-parameterize.html  
Sample data used - https://www.kaggle.com/spscientist/students-performance-in-exams

# Requirements
```
pandas
matplotlib
seaborn
zipfile
papermill
pdfkit
```
These can all be installed via `conda` or `pip`  


`wkhtmltopdf`
Is provided but you can manually install via https://wkhtmltopdf.org/downloads.html which will be installed to `C:\Program Files\wkhtmltopdf`.


# Files
`Basic Commands` - a notebook of assorted tips/extras I've used 
`papermill` - a basic notebook which includes a download / unzip function for datasets on kaggle. This notebook serves as a **workflow** for some dataset (student performances in an exam given gender, education level and *lunch?*). It aims to output a few basic histograms of math, reading and writing results given specified `parameters`. These `parameters` are:
    - `gender`: `["male", "female"]`
    - `edu`: `["associate's degree", "bachelor's degree", 'high school', "master's degree", 'some college', 'some high school']`
`exec_params` - the notebook which (given params) will execute `papermill.ipynb` with the specified parameters. An alternative can be used via terminal command: 
```papermill papermill.ipynb \
          papermill_output.ipynb \
          -p gender 'female' edu "master's degree"
```

> there should be a `.html` output if it works in the `reports` folder. The `exec_params` has already been run but can be changed