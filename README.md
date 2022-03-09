# CoflowLib
CoflowLib is a library of test instances for coflows in datacenter networks

Format of each instance:

```
0				       # identifier of network trace ('0': synthetic, '1': facebook)
2 				     # nb of coflows

1  1 0  5  2	 # coflow id - coflow_weight - coflow_arrival_time - coflow_deadline - num_flows
11  3  2  0 3	 # flow_id - flow_volume - flow_used_ports - flow_ingress - flow_egress
12  4  2  2 4

2  1 3  9  3
21  3  2  0 4
22  4  2  1 3
23  4  2  2 5

6 				     # nb of fabric ports
0 1.0 			   # port_id - port_capacity	
1 1.0
2 1.0
3 1.0
4 1.0
5 1.0
```

CoflowLib
|

|
