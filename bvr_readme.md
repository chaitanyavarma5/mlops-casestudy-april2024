
Create Environment 

```
conda create -n wineq python=3.8 -y
conda activate wineq
```

Create requirements.txt


```
dvc
dvc[gdrive]
scikit-learn

```

```
pip install -r requirements.txt

```


Create template.py 

```
import os

dirs = [
    os.path.join("data", "raw"),
    os.path.join("data", "processed"),
    "notebooks",
    "saved_models",
    "src",
    "data_given"
]

for dir_ in dirs :
    os.makedirs(dir_, exist_ok=True)
    with open(os.path.join(dir_, ".gitkeep"), "w") as f :
        pass

files = [
    "dvc.yaml",
    "params.yaml",
    ".gitignore",
    os.path.join("src", "__init__.py")
]


for file_ in files :
    with open(file_, "w") as f :
        pass

```

```
python template.py

Observe project directory structure has been created 


```