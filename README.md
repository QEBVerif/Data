# QEBVerif: Quantization Error Bound Verification of Neural Networks

This is the official webpage for paper *QebVerif: Quantization Error Bound Verification of Neural Networks*. In this paper, we make the following main contributions:
- We introduce a sound, complete and efficient quantization error bound verification method QebVerif by combining a DRA and an MILP-based verification method;
- We propose a novel DRA to compute sound and tight quantization error intervals accompanied by an abstract domain for QNNs, which can significantly and soundly tighten the quantization error intervals;
- We implement \tool as an end-to-end tool and empirically evaluate QebVerif on a large set of verification tasks and demonstrate its effectiveness and efficiency.

Note that, all the 4 DNNs shown in Table 1 from paper are given in the folder `./benchmark/minist`, and all the experimental raw datum are collected in csv files given in folder  `./Experimental Results`.
- Raw datum of Table 2 are given in `./Experimental Results/RQ_1.csv`;
- Raw datum of Table 3 are given in `./Experimental Results/RQ_2.csv`;
- Raw datum of Figure 4 are given in `./Experimental Results/RQ_3.csv`.

## Benchmarks in Sections 5.2 & 5.3 & 5.4:

The 30 correctly predicted samples from MNIST dataset by all the 20 networks (shown by IDs):

```
3236 5656 7219 7098 3825  521 9886 7389 3064 4544 
7773 1340 7894 8463 6930 2898 2190 1866  914 5574
3770 3016 6395 2897 8541 5082 3712  150 2486 3986
```
