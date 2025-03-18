# DVRP-FPTW-instances
In this repository, there are benchmark instances to test the DVRPFPTW.

## Dependencies
Works with Python 3.8+ and only depends on numpy.

## Example usage

To read the instances you must import numpy library for Python and follow the next procedure:
```python
import numpy as np

# Read Static benchmark instance and solution
static_instance = np.load(instance_file, allow_pickle='TRUE').item()
static_solution = np.load(instance_file_sol, allow_pickle='TRUE').item()
```

`instance` and `solution` are dictionaries that contain all parsed data. 
``` python
>>> static_instance.keys()
dict_keys(['name', 'n_customers', 'node_coord', 'demand', 'service_time', 'edge_weight', 'revenue', 'vehicles', 'capacity', 'autonomy', 'time_window'])

>>> static_solution.keys()
dict_keys(['Name', 'Routes', 'Min_profit', 'Total_profit'])
```
``` python
# Read Dynamic benchmark instance and solution 
dynamic_instance = np.load(dynamic_instance_file, allow_pickle='TRUE').item()
dynamic_solution = np.load(dynamic_instance_file_sol, allow_pickle='TRUE').item()

>>> dynamic_instance.keys()
dict_keys(['name', 'static_instance', 'static_solution', 'event'])

>>> dynamic_instance["event"] 
{'type': 'Vehicle_breakdown',
 'broken_vehicle': 'vehicle_12',
 'broken_time': 28.178005607210743}
```

