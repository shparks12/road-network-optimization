# Road Network Optimization

This repository includes:
- Pickle files of 35 G_tot and 35 G_C* testing instances.
- Visualizations of all 70 testing instances.
- Visualization of all 140 networks produced by the 1-LSNDP-C and 1-LSNDP-I with warm start.

## Reading network instances
To read network instances in Python, use the following code:

```python
import pickle

graph_instance = pickle.load(open(file, 'rb'))  # 'file' should be the path to the pickled network file
```
## Network file naming convention
Each network is given a unique name of form "G_complete_V_X.pickle" or "G_circuity_controlled_V_X.pickle" where "V" is the number of nodes in the network and "X" is the number of the network instance with that number of nodes from 1 to 5. 

## Network properties
Each network object is a NetworkX DiGraph with the following node and edge attributes:

### Node attributes
- 'x': Horizontal position coordinate
- 'y': Vertical position coordinate

### Edge attributes
- 'length': Euclidean distance attribute between node i and node j for edge (i, j). 
