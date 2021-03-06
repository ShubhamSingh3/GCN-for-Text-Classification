# text_gcn

Built a single heterogeneous graph for a corpus based on word co-occurrence and document word relations.
Learned word and document embedding and turned this text classification into node classification



## Require

Python 2.7 or 3.6

Tensorflow >= 1.4.0

## Reproducing Results

1. Run `python remove_words.py 20ng`

2. Run `python build_graph.py 20ng`

3. Run `python train.py 20ng`

4. Change `20ng` in above 3 command lines to `R8`, `R52`, `ohsumed` and `mr` when producing results for other datasets.

## Example input data

1. `/data/20ng.txt` indicates document names, training/test split, document labels. Each line is for a document.

2. `/data/corpus/20ng.txt` contains raw text of each document, each line is for the corresponding line in `/data/20ng.txt`

3. `prepare_data.py` is an example for preparing your own data, note that '\n' is removed in your documents or sentences.

## Inductive version

An inductive version of Text GCN is [fast_text_gcn](https://github.com/yao8839836/fast_text_gcn), where test documents are not included in training process.
