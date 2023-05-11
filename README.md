This repo includes the benchmark data of the paper 'Enhancing Datalog Reasoning with Weighted Hypertree Decomposition' that is accepted by the main track of IJCAI 2023.
The data description is shown below:
* executable/ (containing the executable files of our methods)
* LUBM/ (containing the rules and data of LUBM)
  * LUBM-500-split* (the subsections of LUBM-500.nt.tar.bz2)
  * LUBM_L.dlog (LUBM L rules)
  * LUBM_L-C.dlog (LUBM L+C rules)
* Expressions/ (containing the rules and data of Expression dataset)
  * exp300.nt.tar.bz2 (the data of Expressions)
  * exp-rules.dlog (the rules of Expressions)
* YAGO/ (containing the rules of YAGO)
  * yago_rules.dlog (the rules of YAGO)
  * for the datasets of YAGO, please find it here https://github.com/yspark-dblab/gcare. We use the GCARE-version of YAGO directly. 
  
To decompress exp300.nt.tar.bz2, please use the code below:
```
tar -vxjf exp300.nt.tar.bz2
```

To decompress the LUBM-500 dataset, please use the code below:
```
cat LUBM-500-split* > LUBM-500.nt.tar.bz2
tar -vxjf LUBM-500.nt.tar.bz2
```

To reproduce the experiment results, please refer to the instructions below.
- Step1: Run "./EXE -shell" in command line, in which EXE means one of the executable files in the "executable" directory.
- Step2: Run the following commands:
```
init par-complex-nn
set reason.use-DRed true
import 'RULES.dlog'
mat 
import + 'DATA.nt'
mat (initial materialisation)
import - "DATA_TO_BE_DELETED.nt"
mat (incremental materialisation, deletion)
import + "DATA_TO_BE_DELETED.nt"
mat (incremental materialisation, addition)
```

For instructions of constructing "DATA_TO_BE_DELETED.nt" files, please refer to "DATA_TO_BE_DELETED.nt".
