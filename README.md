# Skip Connections and Training Cost Reduction: A Game Changer in  Graph Neural Networks 

This repository contains a PyTorch implementation of "Skip Connections and Training Cost Reduction: A Game Changer in Graph Neural Networks".

## Dependencies
- CUDA 10.1
- python 3.6.9
- pytorch 1.3.1
- networkx 2.1
- scikit-learn

## Datasets

The `data` folder contains three benchmark datasets(Cora, Citeseer, Pubmed), and the `newdata` folder contains four datasets(Chameleon, Cornell, Texas, Wisconsin) from [Geom-GCN](https://github.com/graphdml-uiuc-jlu/geom-gcn). We use the full-supervised setting as [GCN](https://github.com/tkipf/gcn).

## Results
FULL SUPERVISED EXPERIMENTAL RESULTS FOR MEAN CLASSIFICATION ACCURACY AND TRAINING COST FOR NODE CLASSIFICATION
| Dataset | Training Cost(s)|  Accuracy | Dataset | Training Cost |  Accuracy |
|:---:|:---:|:---:|:---:|:---:|:---:|
| Cora       | **480.00** | 88.03  | Cham | **79.6865**  | **67.43** |
| Cite       | 269.95 | **76.99**  | Corn | **185.32** | **74.59** |
| Pubm       | **3168.37** | **67.43**  | Texa | 369.5642 | **79.46** |
| Wisc | **104.89** | 77.06 |



## Usage

- To replicate the semi-supervised results, run the following script
```sh
sh semi.sh
```
- To replicate the full-supervised results, run the following script
```sh
sh full.sh
```
- To replicate the inductive results of PPI, run the following script
```sh
sh ppi.sh
```
## Reference implementation
The `PyG` folder includes a simple *PyTorch Geometric* implementation of GCNII.
Requirements: `torch-geometric >= 1.5.0` and  `ogb >= 1.2.0`.
- Running examples
```
python cora.py
python arxiv.py
```
