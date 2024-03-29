# NeuroDebug-2_Dataset - Debugging Debug Information With Neural Networks
This repository contains the dataset for NeuroDebug-2: a framework to idenitfy debug information bugs in llvm compiler. You can find our dataset [here](https://drive.google.com/drive/folders/1lEu7vHqIlgBpOe3WKC1a2cH769CQBudo?usp=sharing).

If you use this dataset please cite our Paper.

> @article{NeuroDebug2,
  author={Artuso, Fiorella and Di Luna, Giuseppe Antonio and Querzoni, Leonardo},
  journal={IEEE Access}, 
  title={Debugging Debug Information With Neural Networks}, 
  year={2022},
  volume={10},
  number={},
  pages={54136-54148},
  doi={10.1109/ACCESS.2022.3176617}}

# Dataset Description
You can find four directories:
- [unlabelled_traces](https://drive.google.com/drive/folders/1Rrsq7dscfJflIXzMoOilJrqXH4ztPBIO?usp=sharing): it contains train and validation source traces (`slnet/train_slnet.csv` and `slnet/val_slnet.csv`) and train and validation asm-source mappings (`mapnet/train_mapnet.csv` and `mapnet/val_mapnet.csv`).
-  [synthetic_bugs_traces](https://drive.google.com/drive/folders/1ESYhab5W0ujqJLuQFe_QW63Oqe9dgKMJ?usp=sharing): it contains synthetic-bugged and not bugged source traces (`slnet.csv`) and asm-source mappings (`mapnet.csv`) that we used to test our network.
- [real_bugs_traces](https://drive.google.com/drive/folders/1FAY_uiNi3j3MXxzb1goTdXLnpJLPgv1Y?usp=sharing): it contains real-bugged and not bugged source traces (`slnet.csv`) and asm-source mappings (`mapnet.csv`) that we used to test our network.
- [bugs_discovery_traces](https://drive.google.com/drive/folders/1VxNkEnFvHgSKpEJ-aOIKQApQB-FYj4m4?usp=sharing): it contains  source traces (`slnet.csv`) and asm-source mappings (`mapnet.csv`) that we used to discover new bugs.

csv files contains tab separated pandas dataframes that can be loaded as it follows:
``` python
p = pd.read_csv("train_mapnet.csv", sep="\t")
```
