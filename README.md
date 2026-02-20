# Road Network Optimization

This repository provides graph instance objects and visualizations input to synthetic road network optimization models and visualizations of optimized networks. The method is composed of two mathematical programs: the Linearized One-Level Synthetic Network Design Problem for Circuity Control (1-LSNDP-C) and for Inefficiency Control (1-LSNDP-I).

It includes:
- Pickle files of 35 G_tot and 35 G_C* testing instances, where G_tot instances are input to the 1-LSNDP-C and G_C* instances are input to the 1-LSNDP-I.
- Visualizations of all these 70 testing instances.
- Visualization of all 70 networks produced by the 1-LSNDP-C with warm start and all 70 produced by the 1-LSNDP-I with warm start.

## Reading network instances
To read network instances in Python, use the following code:

```python
import pickle

graph_instance = pickle.load(open(file, 'rb'))  # 'file' should be the path to the pickled network file
```
## Network file naming convention
Each network object is given a unique name of form "G_complete_V_X.pickle" (G_tot instance) or "G_circuity_controlled_V_X.pickle" (G_C* instance) where "V" is the number of vertices in the network and "X" is the number of the network instance with a given vertex count in [1, 5]. 

## Network instance properties
Each network instance object G_tot or G_C* is a NetworkX DiGraph with the following node and edge attributes:

### Vertex attributes
- 'x': Horizontal position coordinate
- 'y': Vertical position coordinate

### Arc attributes
- 'length': Euclidean distance attribute between vertex i and vertex j for arc (i, j).
