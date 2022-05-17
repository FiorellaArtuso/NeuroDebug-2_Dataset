# NeuroDebug-2_Dataset
This repository contains the dataset for NeuroDebug-2: a framework to idenitfy debug information bugs in llvm compiler. You can find our dataset [here](https://drive.google.com/drive/folders/1lEu7vHqIlgBpOe3WKC1a2cH769CQBudo?usp=sharing) and our code [here](https://github.com/FiorellaArtuso/NeuroDebug-2)

# Dataset Description
You can find four directories:
- [unlabelled_traces](https://drive.google.com/drive/folders/1Rrsq7dscfJflIXzMoOilJrqXH4ztPBIO?usp=sharing): it contains train and validation source traces (train_slnet.csv and val_slnet.csv) and train and validation asm-source mappings (train_mapnet.csv and val_mapnet.csv).
-  [synthetic_bugs_traces](https://drive.google.com/drive/folders/1ESYhab5W0ujqJLuQFe_QW63Oqe9dgKMJ?usp=sharing): it contains synthetic-bugged and not bugged source traces (slnet.csv) and asm-source mappings (mapnet.csv) that we used to test our network.
- [real_bugs_traces](https://drive.google.com/drive/folders/1FAY_uiNi3j3MXxzb1goTdXLnpJLPgv1Y?usp=sharing): it contains real-bugged and not bugged source traces (slnet.csv) and asm-source mappings (mapnet.csv) that we used to test our network.
- [bugs_discovery_traces](https://drive.google.com/drive/folders/1VxNkEnFvHgSKpEJ-aOIKQApQB-FYj4m4?usp=sharing): it contains  source traces (slnet.csv) and asm-source mappings (mapnet.csv) that we used to discover new bugs.

csv files contains tab separated pandas dataframes that can be loaded as it follows:
``` python
p = pd.read_csv("train_mapnet.csv", sep="\t")
```
