# StatisticalLoadFiltering

## Abstract: 
Short-term electric load forecasting (STLF) plays an increasingly important role in dispatching power-flow, designing and planning the operation of power systems. To enhance the accuracy of STLF, time series approaches and other intelligent methods are strongly exploited in recent load forecasting models in distribution networks. In developing countries, the load demand in a distribution network can be suddenly changed by power consumption from different customers, e.g. industrial customers, residential customers, so the dataset of load power is often contaminated. Reliability assessment of this dataset is necessary for the pre-processing of previous filtering methods. This paper introduces a novel filtering method that takes into account the reliability of the dataset by analyzing a wide range of confidence levels in comparison with other filtering methods (e.g. Kalman filter, Density-Based Spatial Clustering of Applications with Noise (DBSCAN), Wavelet transform and Singular Spectrum Analysis (SSA)). Real-data load forecasting experiments from more than 50 trustable Supervisory Control and Data Acquisition (SCADA) systems of a typical distribution network in Vietnam are conducted with a neural network model (Artificial Neural Network (ANN)) and a conventional statistical model (Autoregressive Integrated Moving Average (ARIMA)) to validate the proposed novel filtering method. The results demonstrate that STLF using ANN and ARIMA pre-processed with the proposed filtering method at 95% confidence level outperforms the listed filtering methods.

## Table 1. MAPEs (%) of ANN without and with different filtering methods
	      No filter	Proposed, with a 95% confidence level	Kalman filter	DBSCAN	DWT (high frequency signal is removed)	SSA
Sunday	7.92	    6.02	                                      6.45	   7.72	              6.88	                      7.44
Monday	9.65	    5.87	                                      8.22	   8.45	              9.14	                      9.00
Rests   7.06	    5.87	                                      6.72	   6.87	              7.00	                      6.70

## Table 2. MAPEs (%) of ARIMA with regards to different filtering methods
	      No filter	Proposed, with a 95% confidence level	Kalman filter	DBSCAN	DWT (remove high frequency signal)	SSA
Sunday	12.83	    9.89	                                     17.47	   12.65	            16.73	                  12.92
Monday	24	      15.32	                                     24.21     24.22	            24.75	                  24.15
Rests	  21.76	    4.9                                      	 19.99	   21.76	            20.00	                  20.84

Code and files for the evaluation of our proposed method
