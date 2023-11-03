<h1 align="center">
Motif Graph Neural Network 🔥
</h1>

This is a PyTorch implementation of paper: [Motif Graph Neural Network](https://arxiv.org/pdf/2112.14900.pdf)

#### Authors: Xuexin Chen, Ruichu Cai, Yuan Fang, Min Wu, Zijian Li, Zhifeng Hao

### Requirements
- Python == 3.8
- PyTorch == 1.12.1
- DGL == 0.9.0
- PyTorch Geometric == 1.7.2
- NumPy == 1.18.0
- SciPy == 1.6.2

### Repository Structure
- MGNN/data/GraphMGNN_DATA/: datasets for graph classification
  - ./AIDS/raw: original dataset of AIDS
  - ./AIDS/processed: processed dataset of AIDS
  - ./ProcessedMotif.7z: processed motif data of AIDS, ENZYMES and MUTAG.

The introduction of ./ENZYMES and ./MUTAG is the same as above.

- MGNN/data/NodeMGNN_DATA/: datasets for node classification
  - ./Cora/raw: original dataset of Cora
  - ./Cora/processed: processed dataset of Cora
  - ./processed/motif_adj4Cora: contain 13 motif-based adjacency matrices of Cora

The introduction of ./CiteSeer, ./PubMed and ./chem2bio2rdf is the same as above.

- MGNN/MGNN_Graph/: graph classification code of MGNN
  - layer.py: implementation of a MGNN layer
  - preprocess.py: build 13 motif adjacency matrices for each graph
  - utils.py: implementation of building 13 motif adjacency matrices for a graph and other utility functions
  - main.py: MGNN implementation, training and evaluation

- MGNN/MGNN_Node/: node classification code of MGNN on Cora, Citeseer and Pubmed
  - layer.py: implementation of a MGNN layer
  - utils.py: implementation of building 13 motif adjacency matrices for a graph and other utility functions
  - main.py:  MGNN implementation, training and evaluation
 
- MGNN/MGNN_CBR/: node classification code of MGNN on Chem2Bio2RDF and the introduction of its subdirectory is the same as MGNN/MGNN_Node/.

### How to run our code
1. **Please unzip all 7z files to their directory first.**

within MGNN/

2. For graph classification task, run the following scripts: ./MGNN_Graph/main.py 
3. For node classification task, run the following scripts:
- on Cora, Citeseer and Pubmed: ./MGNN_Node/main.py 
- on Chem2Bio2RDF: ./MGNN_CBR/main.py

# Citation
If you find this code useful, please cite the following:
```
@ARTICLE{10154572,
  author={Chen, Xuexin and Cai, Ruichu and Fang, Yuan and Wu, Min and Li, Zijian and Hao, Zhifeng},
  journal={IEEE Transactions on Neural Networks and Learning Systems}, 
  title={Motif Graph Neural Network}, 
  year={2023},
  volume={},
  number={},
  pages={1-15},
  doi={10.1109/TNNLS.2023.3281716}}
```

