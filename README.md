### View [this nbviewer mirrored repository](https://nbviewer.org/github/kanru-wang/Graph_Neural_Network), if you see formatting issues in the notebooks above.

--------------------------------

<br>

# Graph Neural Network

Source:
- https://snap.stanford.edu/class/cs224w-2023/
- https://www.youtube.com/playlist?list=PLoROMvodv4rPLKxIpqhjhPgdQy7imNkDn
- https://pytorch-geometric.readthedocs.io/en/latest/get_started/colabs.html

## Chapter 3. Node Embeddings (Shallow encoding: Deepwalk and Node2Vec)
<img src="image/image001.png" width="800"/>
<img src="image/image002.png" width="800"/>
<img src="image/image003.png" width="800"/>
<img src="image/image004.png" width="800"/>

## Chapter 5. Label Propagation for Node Classification

- Relational classification: Propagate node labels across the network. Iteratively update probabilities of node belonging to a label class based on its neighbors.
- Iterative Classification: Tabulate the incoming / outcoming predicted label information. Then train a classifier to classify each node based on its features as well as labels of neighbors; do that iteratively.
- Correct & Smooth

## Chapter 6. Graph Neural Networks 1: GNN Model

Can solve:
- Node classification - Predict a type of a given node
- Link prediction - Predict whether two nodes are linked
- Community detection - Identify densely linked clusters of nodes
- Network similarity - How similar are two (sub)networks

Average neighbor’s previous layer embeddings and matrix multiply the weights. So as long as the embedding length is fixed, the model can handle any number of neighbors.

<img src="image/image055.png" width="550"/>
<img src="image/image056.png" width="400"/>
<img src="image/image057.png" width="400"/>
<img src="image/image058.png" width="600"/>

-	CNN can be seen as a special GNN with fixed neighbor size and ordering.
-	The size of the filter is pre-defined for a CNN.
-	The advantage of GNN is it processes arbitrary graphs with different degrees for each node.
-	CNN is not permutation equivariant. Switching the order of pixels will lead to different outputs.

<img src="image/image061.png" width="400"/>

## Chapter 7. Graph Neural Networks 2: Design Space

### Attention Mechanism

<img src="image/image063.png" width="400"/>
<img src="image/image064.png" width="450"/>
<img src="image/image065.png" width="500"/>
<img src="image/image066.png" width="550"/>

## Chapter 8. Applications of Graph Neural Networks

<img src="image/image067.png" width="400"/>
<img src="image/image068.png" width="400"/>
<img src="image/image069.png" width="400"/>
<img src="image/image070.png" width="450"/>
<img src="image/image071.png" width="450"/>
<img src="image/image072.png" width="450"/>
<img src="image/image073.png" width="450"/>
<img src="image/image074.png" width="500"/>

<br>

## Chapter 10. Knowledge Graph Embeddings

<img src="image/image075.png" width="450"/>
<img src="image/image076.png" width="550"/>
<img src="image/image077.png" width="450"/>

### Example: Link Prediction

<img src="image/image079.png" width="500"/>
<img src="image/image080.png" width="500"/>
<img src="image/image081.png" width="550"/>

<br>

## Chapter 13. GNNs for Recommender Systems

<img src="image/image082.png" width="450"/>
<img src="image/image083.png" width="400"/>

### Binary Loss

<img src="image/image084.png" width="350"/>
<img src="image/image085.png" width="450"/>
<img src="image/image086.png" width="350"/>

### Bayesian Personalized Ranking (BPR) Loss

Bayesian Personalized Ranking (BPR) Loss is a personalized surrogate loss that aligns better with the recall@K metric.

<img src="image/image088.png" width="550"/>
<img src="image/image089.png" width="450"/>
<img src="image/image090.png" width="400"/>
<img src="image/image091.png" width="400"/>
<img src="image/image092.png" width="400"/>
<img src="image/image093.png" width="400"/>
<img src="image/image094.png" width="550"/>
<img src="image/image095.png" width="220"/>
<img src="image/image096.png" width="500"/>
<img src="image/image097.png" width="450"/>
<img src="image/image098.png" width="500"/>

- LightGCN simplifies NGCF by removing the learnable parameters of GNNs.
- Learnable parameters are all in the shallow input node embeddings.

<img src="image/image100.png" width="450"/>
