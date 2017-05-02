# Python code for the baseline graph partition algorithm
For clarity and simplicity, here is a pure Python implementation of the baseline algorithm. Runtime-wise, it is about an order of magnitude slower than the C++ implementation.

## Source code

### Jupyter notebook file
- partition_baseline.ipynb : Contains the entire implementation, with documentation on the algorithmic details of each step of the algorithm. Run this to visualize and see the intermediate results through each step of the graph partitioning algorithm, to get a feel for how it works.

### Python files
- partition_baseline_support.py : Source code for all the supporting functions of the graph partitioning algorithm, with functional documentation detailiong all the inputs and outputs 

- partition_baseline_main.py : Source code for the main routine that invokes the supporting functions to perform graph partitioning. Arguments may be passed to specify the data set and streaming stage to process. For example: "python partition_baseline_main.py ../../data/static/simulated_blockmodel_graph_5000_nodes" partitions the static graph with 5000 nodes and "python partition_baseline_main.py ../../data/streaming/emergingEdges/500_nodes/simulated_blockmodel_graph_500_nodes_edgeSample -p 7" partitions stage 7 of the streaming graph with emerging edges.

## Version
The source code is run and tested using Python 2.7

## Dependency
This baseline implementation uses the following Python modules:

### Required modules (standard or easy to install)
- pandas : for loading input graph TSV files

- numpy : used extensively for storage and computations

- scipy : for sparse matrix and some specific computations

- munkres : linear assignment module for computing the correctness metrics, by Brian Clapper (https://pypi.python.org/pypi/munkres/)

### Optional modules
- timeit : for timing each run (https://docs.python.org/2/library/timeit.html)

- graph_tool : for visualizing the intermediate partitioning results (https://graph-tool.skewed.de/). Tested with v.2.16.

