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
## Verification Results in Table 2:

#### Verification Results with DRA only for P1:

| Quantization      | Verification Results (error = 1) | Verification Results (error = 2) | Verification Results (error = 4) | Verification Results (error = 6) |Verification Results (error = 8) |
| :-----  | :-------      | :-------      | :-------      | :-------      | :-------      |
| Q = 4   | Proved (0)    | Proved (2)    | Proved (26)   | Proved (30)   | Proved (30)   | 
|         | Unknown (150) | Unknown (148) | Unknown (124) | Unknown (120) | Unknown (120) |
| Q = 6   | Proved (15)   | Proved (26)   | Proved (29)   | Proved (30)   | Proved (30)   | 
|         | Unknown (135) | Unknown (124) | Unknown (121) | Unknown (120) | Unknown (120) |
| Q = 8   | Proved (21)   | Proved (26)   | Proved (29)   | Proved (30)   | Proved (30)   | 
|         | Unknown (129) | Unknown (124) | Unknown (121) | Unknown (120) | Unknown (120) |
| Q = 10  | Proved (24)   | Proved (26)   | Proved (29)   | Proved (30)   | Proved (30)   | 
|         | Unknown (126) | Unknown (124) | Unknown (121) | Unknown (120) | Unknown (120) |

#### Verification Results with DRA only for P2:

| Quantization      | Verification Results (error = 1) | Verification Results (error = 2) | Verification Results (error = 4) | Verification Results (error = 6) |Verification Results (error = 8) |
| :-----  | :-------      | :-------      | :-------      | :-------      | :-------      |
| Q = 4   | Proved (0)    | Proved (0)    | Proved (2)    | Proved (18)   | Proved (29)   | 
|         | Unknown (150) | Unknown (150) | Unknown (148) | Unknown (132) | Unknown (121) |
| Q = 6   | Proved (0)    | Proved (4)    | Proved (24)   | Proved (30)   | Proved (30)   | 
|         | Unknown (150) | Unknown (146) | Unknown (126) | Unknown (120) | Unknown (120) |
| Q = 8   | Proved (2)    | Proved (18)   | Proved (28)   | Proved (30)   | Proved (30)   | 
|         | Unknown (148) | Unknown (132) | Unknown (122) | Unknown (120) | Unknown (120) |
| Q = 10  | Proved (4)    | Proved (20)   | Proved (28)   | Proved (30)   | Proved (30)   | 
|         | Unknown (146) | Unknown (130) | Unknown (122) | Unknown (120) | Unknown (120) |

#### Verification Results with DRA only for P4:

| Quantization      | Verification Results (error = 1) | Verification Results (error = 2) | Verification Results (error = 4) | Verification Results (error = 6) |Verification Results (error = 8) |
| :-----  | :-------      | :-------      | :-------      | :-------      | :-------      |
| Q = 4   | Proved (0)    | Proved (0)    | Proved (0)    | Proved (0)    | Proved (1)    | 
|         | Unknown (150) | Unknown (150) | Unknown (150) | Unknown (150) | Unknown (149) |
| Q = 8   | Proved (0)    | Proved (4)    | Proved (23)   | Proved (29)   | Proved (30)   | 
|         | Unknown (150) | Unknown (146) | Unknown (127) | Unknown (121) | Unknown (120) |
