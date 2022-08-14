This repo includes the benchmark data of the paper 'Enhancing Datalog Reasoning with Weighted Hypertree Decomposition' that is submitted to the main track of AAAI 2023.
The data description is shown below:
* LUBM/ (containing the rules and data of LUBM)
  * LUBM-500-split* (the subsections of LUBM-500.nt.tar.bz2)
  * LUBM_L.dlog (LUBM L rules)
  * LUBM_L-C.dlog (LUBM L+C rules)
* Expressions/ (containing the rules and data of Expression dataset)
  * exp300.nt.tar.bz2 (the data of Expressions)
  * exp-rules.dlog (the rules of Expressions)

To decompress exp300.nt.tar.bz2, please use the code below:
```
tar -vxjf exp300.nt.tar.bz2
```

To decompress the LUBM-500 dataset, please use the code below:
```
cat LUBM-500-split* > LUBM-500.nt.tar.bz2
tar -vxjf LUBM-500.nt.tar.bz2
```
