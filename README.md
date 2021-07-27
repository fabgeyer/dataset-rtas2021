# Tightening Network Calculus Delay Bounds by Predicting Flow Prolongations in the FIFO Analysis

This repository contains the dataset used for the paper [_"Tightening Network Calculus Delay Bounds by Predicting Flow Prolongations in the FIFO Analysis"_](https://doi.org/10.1109/RTAS52030.2021.00021) publish at the [27th IEEE Real-Time and Embedded Technology and Applications Symposium (RTAS 2021)](http://2021.rtas.org/). We refer to the paper for a full explanation of the methodology used for generating the dataset.


## Citation

If you use this dataset for your research, please include the following reference in any resulting publication:

```bibtex
@inproceedings{GeyerSchefflerBondorf_RTAS2021,
	author    = {Geyer, Fabien and Scheffler, Alexander and Bondorf, Steffen},
	title     = {Tightening Network Calculus Delay Bounds by Predicting Flow Prolongations in the {FIFO} Analysis},
	booktitle = {Proceedings of the 27th IEEE Real-Time and Embedded Technology and Applications Symposium (RTAS 2021)},
	year      = {2021},
	month     = may,
	doi       = {10.1109/RTAS52030.2021.00021},
}
```


## Getting the dataset

The raw dataset can be accessed via the DOI: [10.14459/2020mp1596901](https://doi.org/10.14459/2020mp1596901).
The following command can be used to download the full dataset via FTP:
```
$ wget -r ftp://m1596901:m1596901@dataserv.ub.tum.de/
```

The dataset is comprised of three files:

- `dataset-train.pbz` is the dataset used for training the GNN
- `dataset-evaluation.pbz` is the dataset used for evaluation in Section VI, except for Subsection VI-C
- `dataset-evaluation-large.pbz` is the dataset used for evaluation in Section VI-C

Additionally, `dataset_structure.proto` details the datastructure used for the dataset.

## Reading the dataset

The dataset is stored as serialized protobuf messages using the Python library [pbzlib](https://github.com/fabgeyer/pbzlib-py).
Alternative programming languages may be used with `pbzlib` (e.g. [Java](https://github.com/fabgeyer/pbzlib-java), [Go](https://github.com/fabgeyer/pbzlib-go)).

This repository contains an [example python script](https://github.com/fabgeyer/dataset-rtas2021/blob/master/example.py) for parsing the files.
To get it and execute it:
```
$ git clone https://github.com/fabgeyer/dataset-rtas2021.git
$ cd dataset-rtas2021
$ pip3 install --upgrade pbzlib
$ python3 example.py path/to/dataset-train.pbz
```

## License

The data in this repository is licensed under [Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)](http://creativecommons.org/licenses/by-sa/4.0).
