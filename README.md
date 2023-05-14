# DVRP-PFPTW-instances
In this repostory there are the benchmark instances to test the DVRPFPTW.

## Dependecies
Works with Python 3.8+ and only depends on numpy.
## Example usage


To read the instances you must import numpy libary for python and following the next procedure:
```python
import numpy as np

# Read benchamark instance and solution
instance = np.load(instance_file, allow_pickle='TRUE').item()
solution = np.load(instance_file_sol, allow_pickle='TRUE').item()
```

`instance` and `solution` are dictionaries that contain all parsed data. 
``` python
>>> instance.keys()
dict_keys(['name', 'n_customers', 'node_coord', 'demand', 'service_time', 'edge_weight', 'revenue', 'vehicles', 'capacity', 'autonomy', 'time_window'])

>>> solution.keys()
dict_keys(['Name', 'Routes', 'Min_profit', 'Total_profit'])
```
