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
## Verification Results (number of verified, unknown(UK)/timeout(TO) tasks) in Table 2:

#### Verification Results for P1:

<table>
  <tr>
      <th rowspan="2">Quantization</th><th rowspan="2">Results</th>
      <th colspan="3">Verification Results (error = 1)</th>
      <th colspan="3">Verification Results (error = 2)</th>
      <th colspan="3">Verification Results (error = 4)</th>
      <th colspan="3">Verification Results (error = 6)</th>
      <th colspan="3">Verification Results (error = 8)</th>
  </tr>
  <tr>
      <td>DRA</td><th>DRA+MILP</td><td>DRA+MILP+Diff</td>
      <td>DRA</td><th>DRA+MILP</td><td>DRA+MILP+Diff</td>
      <td>DRA</td><th>DRA+MILP</td><td>DRA+MILP+Diff</td>
      <td>DRA</td><th>DRA+MILP</td><td>DRA+MILP+Diff</td>
      <td>DRA</td><th>DRA+MILP</td><td>DRA+MILP+Diff</td>
  </tr>
  <tr>
      <td rowspan="2">Q=4</td><td>Verified</td><td>0</td>	<td>30</td>	<td>30</td>	<td>2</td>	<td>30</td>	<td>30</td>	<td>26</td>	<td>30</td>	<td>30</td>	<td>30</td><td>30</td>	<td>30</td>	<td>30</td>	<td>30</td>	<td>30</td>
  </tr>
  <tr>
      <td>UK/TO</td><td>30</td>	<td>0</td>	<td>0</td>	<td>28</td>	<td>0</td>	<td>0</td> <td>4</td> <td>0</td> <td>0</td> <td>0</td> <td>0</td> <td>0</td> <td>0</td> <td>0</td> <td>0</td>
  </tr>
  
  <tr>
      <td rowspan="2">Q=6</td><td>Verified</td><td>15</td><td>28</td><td>29</td><td>26</td><td>30</td><td>30</td><td>29</td><td>30</td><td>30</td><td>30</td><td>30</td><td>30</td><td>30</td><td>30</td><td>30</td>
  </tr>
  <tr>
      <td>UK/TO</td><td>15</td><td>2</td><td>1</td><td>4</td><td>0</td><td>0</td><td>1</td><td>0</td><td>0</td><td>0</td><td>0</td><td>0</td><td>0</td><td>0</td><td>0</td>
  </tr>
  
  <tr>
      <td rowspan="2">Q=8</td><td>Verified</td><td>21</td><td>30</td><td>30</td><td>26</td><td>30</td><td>30</td><td>29</td><td>30</td><td>30</td><td>30</td><td>30</td><td>30</td><td>30</td><td>30</td><td>30</td>
  </tr>
  <tr>
      <td>UK/TO</td><td>9</td><td>0</td><td>0</td><td>4</td><td>0</td><td>0</td><td>1</td><td>0</td><td>0</td><td>0</td><td>0</td><td>0</td><td>0</td><td>0</td><td>0</td>
  </tr>
  
  <tr>
      <td rowspan="2">Q=10</td><td>Verified</td><td>24</td><td>30</td><td>30</td><td>26</td><td>30</td><td>30</td><td>29</td><td>30</td><td>30</td><td>30</td><td>30</td><td>30</td><td>30</td><td>30</td><td>30</td>
  </tr>
  <tr>
      <td>UK/TO</td><td>6</td><td>0</td><td>0</td><td>4</td><td>0</td><td>0</td><td>1</td><td>0</td><td>0</td><td>0</td><td>0</td><td>0</td><td>0</td><td>0</td><td>0</td>
  </tr>
  
</table>

#### Verification Results for P2:

<table>
  <tr>
      <th rowspan="2">Quantization</th><th rowspan="2">Results</th>
      <th colspan="3">Verification Results (error = 1)</th>
      <th colspan="3">Verification Results (error = 2)</th>
      <th colspan="3">Verification Results (error = 4)</th>
      <th colspan="3">Verification Results (error = 6)</th>
      <th colspan="3">Verification Results (error = 8)</th>
  </tr>
  <tr>
      <td>DRA</td><th>DRA+MILP</td><td>DRA+MILP+Diff</td>
      <td>DRA</td><th>DRA+MILP</td><td>DRA+MILP+Diff</td>
      <td>DRA</td><th>DRA+MILP</td><td>DRA+MILP+Diff</td>
      <td>DRA</td><th>DRA+MILP</td><td>DRA+MILP+Diff</td>
      <td>DRA</td><th>DRA+MILP</td><td>DRA+MILP+Diff</td>
  </tr>
  <tr>
      <td rowspan="2">Q=4</td><td>Verified</td><td>0</td><td>30</td><td>30</td><td>0</td><td>22</td><td>23</td><td>2</td><td>21</td><td>21</td><td>18</td><td>29</td><td>29</td><td>29</td><td>30</td><td>30</td>
  </tr>
  <tr>
      <td>UK/TO</td><td>30</td><td>0</td><td>0</td><td>30</td><td>8</td><td>7</td><td>28</td><td>9</td><td>9</td><td>12</td><td>1</td><td>1</td><td>1</td><td>0</td><td>0</td>
  </tr>
  
  <tr>
      <td rowspan="2">Q=6</td><td>Verified</td><td>0</td><td>18</td><td>18</td><td>4</td><td>30</td><td>30</td><td>24</td><td>30</td><td>30</td><td>30</td><td>30</td><td>30</td><td>30</td><td>30</td><td>30</td>
  </tr>
  <tr>
      <td>UK/TO</td><td>30</td><td>12</td><td>12</td><td>26</td><td>0</td><td>0</td><td>6</td><td>0</td><td>0</td><td>0</td><td>0</td><td>0</td><td>0</td><td>0</td><td>0</td>
  </tr>
  
  <tr>
      <td rowspan="2">Q=8</td><td>Verified</td><td>2</td><td>25</td><td>27</td><td>18</td><td>30</td><td>29</td><td>28</td><td>30</td><td>30</td><td>30</td><td>30</td><td>30</td><td>30</td><td>30</td><td>30</td>
  </tr>
  <tr>
      <td>UK/TO</td><td>28</td><td>5</td><td>3</td><td>12</td><td>0</td><td>1</td><td>2</td><td>0</td><td>0</td><td>0</td><td>0</td><td>0</td><td>0</td><td>0</td><td>0</td>
  </tr>
  
  <tr>
      <td rowspan="2">Q=10</td><td>Verified</td><td>4</td><td>27</td><td>27</td><td>20</td><td>28</td><td>28</td><td>28</td><td>30</td><td>30</td><td>30</td><td>30</td><td>30</td><td>30</td><td>30</td><td>30</td>
  </tr>
  <tr>
      <td>UK/TO</td><td>26</td><td>3</td><td>3</td><td>10</td><td>2</td><td>2</td><td>2</td><td>0</td><td>0</td><td>0</td><td>0</td><td>0</td><td>0</td><td>0</td><td>0</td>
  </tr>
  
</table>

#### Verification Results for P3:

<table>
  <tr>
      <th rowspan="2">Quantization</th><th rowspan="2">Results</th>
      <th colspan="3">Verification Results (error = 1)</th>
      <th colspan="3">Verification Results (error = 2)</th>
      <th colspan="3">Verification Results (error = 4)</th>
      <th colspan="3">Verification Results (error = 6)</th>
      <th colspan="3">Verification Results (error = 8)</th>
  </tr>
  <tr>
      <td>DRA</td><th>DRA+MILP</td><td>DRA+MILP+Diff</td>
      <td>DRA</td><th>DRA+MILP</td><td>DRA+MILP+Diff</td>
      <td>DRA</td><th>DRA+MILP</td><td>DRA+MILP+Diff</td>
      <td>DRA</td><th>DRA+MILP</td><td>DRA+MILP+Diff</td>
      <td>DRA</td><th>DRA+MILP</td><td>DRA+MILP+Diff</td>
  </tr>
  <tr>
      <td rowspan="2">Q=4</td><td>Verified</td><td>0</td><td>30</td><td>30</td><td>0</td><td>29</td><td>28</td><td>0</td><td>15</td><td>16</td><td>0</td><td>5</td><td>4</td><td>1</td><td>7</td><td>7</td>
  </tr>
  <tr>
      <td>UK/TO</td><td>30</td><td>0</td><td>0</td><td>30</td><td>1</td><td>2</td><td>30</td><td>15</td><td>14</td><td>30</td><td>25</td><td>26</td><td>29</td><td>23</td><td>23</td>
  </tr>
  
  <tr>
      <td rowspan="2">Q=8</td><td>Verified</td><td>0</td><td>17</td><td>19</td><td>4</td><td>17</td><td>27</td><td>23</td><td>28</td><td>29</td><td>29</td><td>30</td><td>30</td><td>30</td><td>30</td><td>30</td>
  </tr>
  <tr>
      <td>UK/TO</td><td>30</td><td>13</td><td>11</td><td>26</td><td>13</td><td>3</td><td>7</td><td>2</td><td>1</td><td>1</td><td>0</td><td>0</td><td>0</td><td>0</td><td>0</td>
  </tr>
  
</table>

- Note that, we happen to collect the verification results of error=0.5(all verified successfully) for methods "DRA+MILP" and  "DRA+MILP+Diff" for P2-4, hence the number of verified tasks in the paper is 30 more than here, i.e., (162 and 163 in paper vs. 132 and 133 here);
- We forget to collect the verification results of method "DRA only" when error=1 for all the networks in the paper;
- We will correct them all in the next version.
