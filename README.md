# Learning-Assisted Inertia Estimation
This set of codes implements our TIA paper "Machine Learning Assisted Inertia Estimation using Ambient Measurements". 


## Introduction:
* The power system has temporal and spatial characteristics, LRCN and GCN based learning algorithms are proposed to estimate system inertia.
* The dataset includes time series profiles of frequency and voltage measurements, the sampling rate of PMU is considered as 200Hz in this work.
* Measuremnts on each generator buses are obtained with graphical information embedded.


## Power system PMU measurements datasets:
* 'train_3rd_wrv.xlsx': measurements of freuqency/RoCoF/voltages magnitude within period 0.0s - 1.0s following the probing signal on each generator bus.
* 'train_3rd_wrv_SNR45db.xlsx': measurements obtained under noisy condition, gaussian distributed noise with SNR at 45dB is added.
* 'train_0.5s_delay.xlsx':freuqency measurements within period 0.5s - 1.5s following the probing signal on each generator bus.
* 'data.dat': nodes and install limits information.

The three excel files are too large to share them on Github. Instead, they are shared on Figshare, along with the raw simulation data. The download link is: 
* https://figshare.com/articles/dataset/Raw_Dataset_for_IEEE_24-Bus_System_Freuqency_Dynamics_Measurements/23576769


## Power system test data:
The test system used in this work is a modified IEEE 24-bus system: one area of the IEEE 73-bus system ("The IEEE Reliability Test System-1996. A report prepared by the Reliability Test System Task Force of the Application of Probability Methods Subcommittee" and link is <a class="" target="_blank" href="https://ieeexplore.ieee.org/document/780914">here</a>).


## Python Codes to train NN models:
* 'DNN_Delay_0.5.ipynb': training and testing of deep neural network (DNN) on dataset 'train_0.5s_delay.xlsx'.
* 'DNN_InertiaEST.ipynb': training and testing of deep neural network (DNN) on dataset 'train_3rd_wrv.xlsx'.
* 'DNN_InertiaEST_45dB.ipynb': training and testing of deep neural network (DNN) on dataset 'train_3rd_wrv_SNR45db.xlsx'.
* 'CNN_Delay_0.5.ipynb': training and testing of convolutional neural network (CNN) on dataset 'train_0.5s_delay.xlsx'.
* 'CNN_InertiaEST.ipynb': define functions to build, solve, and save results for pyomo SCUC model.
* 'CNN_InertiaEST_45dB.ipynb': define functions to build, solve, and save results for pyomo SCUC model.
* 'LRCN_Delay_0.5.ipynb': define the python class for the power system.
* 'LRCN_InertiaEST.ipynb': define functions to build, solve, and save results for pyomo SCUC model.
* 'LRCN_InertiaEST_45dB.ipynb': define functions to build, solve, and save results for pyomo SCUC model.
* 'GNN_Delay_0.5.ipynb': define the python class for the power system.
* 'GNN_InertiaEST.ipynb': define functions to build, solve, and save results for pyomo SCUC model.
* 'GNN_InertiaEST_45dB.ipynb': define functions to build, solve, and save results for pyomo SCUC model.
* 'Optimal_PMU_Allocation.ipynb': optimization problem for optimal PMU allocation with limited resources.


## Python Codes Environment
* Recommand Python Version: Python 3.8
* Required packages: numpy, matplotlib,tensorflow 2.10.0, pytorch_geometrics, pyomo


## Citation:
If you use any of our codes/data for your work, please cite the following two papers as your references:

* Mingjian Tuo and Xingpeng Li, “Long-term Recurrent Convolutional Networks-based Inertia Estimation using Ambient Measurements”, *IEEE IAS Annual Meeting*, Detroit, MI, USA, Oct. 2022.

* Mingjian Tuo and Xingpeng Li, “Machine Learning Assisted Inertia Estimation using Ambient Measurements”, *IEEE Transaction on Industry Applications*, Apr. 2023.

Paper-2 website: <a class="off" href="/papers/MJ-Tuo_ML-Inertia-Est/"  target="_blank">https://rpglab.github.io/papers/MJ-Tuo_ML-Inertia-Est/</a>


## Contributions:
Mingjian Tuo created this dataset and python codes. Xingpeng Li supervised this work.


## Contact:
Dr. Xingpeng Li

University of Houston

Email: xli83@central.uh.edu

Website: <a class="off" href="/"  target="_blank">https://rpglab.github.io/</a>


## License:
This work is licensed under the terms of the <a class="off" href="https://creativecommons.org/licenses/by/4.0/"  target="_blank">Creative Commons Attribution 4.0 (CC BY 4.0) license.</a>


## Disclaimer:
The author doesn’t make any warranty for the accuracy, completeness, or usefulness of any information disclosed; and the author assumes no liability or responsibility for any errors or omissions for the information (data/code/results etc) disclosed.
