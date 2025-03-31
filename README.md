# Rebuttal
Table 1: The experimental results (\%) of various baselines under the data heterogeneity parameter $\alpha$ = 0.5. The datasets of Matek19, Aceve20 and HLwBC in the class incremental learning scenario, and the scenario of FDIL. Other parameter settings: FCIL: $\delta=0.02, a=0.8, \lambda=0.4$; FDIL: $\delta=0.02, a=0.4, \lambda=0.8$.
| FIL      | FCIL_M<br />avg | FCIL_M<br />last | FCIL_A<br />avg | FCIL_A<br />last | FCIL_H<br />avg | FCIL_H<br />last | FDIL<br />avg | FDIL<br />last |
| -------- | --------------- | ---------------- | --------------- | ---------------- | --------------- | ---------------- | ------------- | -------------- |
| iCaRL    | 61.55           | 23.92            | 59.97           | 49.75            | 74.76           | 57.56            | 51.30         | 40.18          |
| UACL     | 61.08           | 23.92            | 59.53           | 51.14            | 71.67           | 49.56            | 51.21         | 46.05          |
| Re-Fed   | 74.36           | 58.62            | 73.22           | 63.57            | 87.04           | 80.49            | 73.86         | 79.28          |
| PILoRA   | 68.15           | 71.78            | 70.67           | 50.90            | 81.24           | 70.46            | 18.27         | 25.54          |
| FedSpace | 47.38           | 21.45            | 24.78           | 11.32            | 27.31           | 13.14            |   -            |   -             |
| our      | 78.32           | 72.06            | 79.77           | 74.00            | 88.48           | 82.95            | 78.53         | 81.02          |

Table 2: Training time: The average training duration for each task; Memory: The average cache load for each client. 
|          | Training Time | Memory(avg) | Memory(Max) | Memory(mix) |
| -------- | ---------------- | ----------- | ----------- | ----------- |
| iCaRL    | 2000s             | 799.15M     | 1050.05M    | 284.06M     |
| UACL     | 2250s            | 815.91M     | 1072.66M    | 326.50M     |
| Re-Fed   | 2400s             | 1108.36M    | 1704.91M     | 283.74M     |
| PILoRA   | 3675s             | 2498.96M    | 3348.53M     | 1110.30M    |
| FedSpace | 3750s             | 248.04M     | 264.42M     | 173.10M     |
| our      | 2450s             | 1288.01M     | 1705.93M    | 283.74M     |

Table 3: In the FCIL-M scenario, the storage space $m_{c,t}$ of the example set dynamically allocated by our method for different clients under different tasks. Here, $c$ represents the client index and $t$ represents the task index. 
| our(m_c,t)            | Task 1 | Task 2 | Task 3 | Task 4 |
| --------------------- | ------ | ------ | ------ | ------ |
| client 1              | 239    | 243    | 346    | 346    |
| client 2              | 241    | 88     | 61     | 61     |
| client 3              | 239    | 184    | 367    | 367    |
| client 4              | 238    | 283    | 122    | 122    |
| client 5              | 238    | 400    | 400    | 400    |
| client 6              | -      | 200    | 102    | 102    |
| client 7              | -      | -      | -      | 200    |
| **Fixed (baselines)** |   **Task 1**  |    **Task 2**     |   **Task 3**      |     **Task 4**    |
| client 1              | 200    | 200    | 200    | 200    |
| client 2              | 200    | 200    | 200    | 200    |
| client3               | 200    | 200    | 200    | 200    |
| client 4              | 200    | 200    | 200    | 200    |
| client 5              | 200    | 200    | 200    | 200    |
| client 6              | -      | 200    | 200    | 200    |
| client 7              | -      | -      | -      | 200    |
