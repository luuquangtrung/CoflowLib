# CoflowLib
CoflowLib is a library of test instances for coflows in datacenter networks


Structure of the repository:
```
CoflowLib
├── offline_instances
│      	├── noweight
│ 	│ 	├── off_facebook_m10_c10.zip
│   	│  	└── ...
│	└── weight
│	 	├── w_off_facebook_m10_c10.zip
│	  	└── ...
└── online_instances
   	├── `batch
 	│ 	├── on_synthetic_batch_m10_c8000_l2.zip
   	│  	└── ...
   	└── nobatch
 	 	├── on_synthetic_nobatch_m10_c2000_l2.zip
  		└── ...
```

CoflowLib contains instances for offline and online simulations.
* `offline_instances` provides instances for offline simulations (i.e., the arrival time of all coflows is set to zero). Coflows may have or do not have weights (respectively in the `weight` and `noweight` folder).
* `online_instances` provides instances for offline simulations. Two scenarios are considered:
	* the first scenario (folder `batch`) is when coflows arrive as a batch each time, with a Poisson distribution of rate `lambda`, the value of `lambda` is indicated in the name of each instance (e.g., `l2` means `lambda = 2`, or `lam0p2` means `lambda = 0.2`);
	* the second scenario (folder `nobatch`) is the basic situation, in which each coflow arrives at a time.


Format of each instance:

```
0	# identifier of network trace ('0': synthetic, '1': facebook)
2 	# nb of coflows

1  1 0  5  2	# coflow id - coflow_weight - coflow_arrival_time - coflow_deadline - num_flows
11  3  2  0 3	# flow_id - flow_volume - flow_used_ports - flow_ingress - flow_egress
12  4  2  2 4

2  1 3  9  3
21  3  2  0 4
22  4  2  1 3
23  4  2  2 5

6	# nb of fabric ports
0 1.0	# port_id - port_capacity	
1 1.0
2 1.0
3 1.0
4 1.0
5 1.0
```


#### Authors
* Quang-Trung Luu
* Cédric Richier
* Rachid El-Azouzi
* Francesco De Pellegrini
* Olivier Brun
* Balakrishna J. Prabhu

(c) 2022 LIA - University of Avignon and LAAS-CNRS

