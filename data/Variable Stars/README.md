# Variable Stars



A variable star changes its intensity, as observed by a telescope, over time. This can be caused extrinsically, for example by other objects temporarily occluding it, but also intrinsically, when the star changes its physical properties over time. Figure 1 shows an example. The graph of the varying intensity as a function of time is called the light curve. Variable stars can be further divided into many classes depending on other physical properties. The task we are trying to solve is to predict the class of a variable star by its light curve. To achieve this, we train a classifier in a supervised setting using labeled data from the *All Sky Automated Survey Catalog of Variable Stars* (ACVS) [Pojmanski, 2000].

The data is based on the study by Richards et al. [2012]. We have a training and a test set, in the file `train.dt` and `test.dt`, respectively, with 771 labeled samples each. Each sample encodes the astronomical properties of a variable star in a 61-dimensional feature vector. The features and classes are listed below, for a detailed description of their meaning we refer to Dubath et al. [2011] and Richards et al. [2011]. 
The data sets `X_train_binary.dt`, `X_test_binary.dt`, `y_train_binary.dt` and `y_test_binary.dt` reduce the data to a binary classification problem.

The labels indicate the class a variable star has been assigned to. In total there are 25 different classes.


## Data set description

#### Input featues

| \# 	| Feature                          	|
|----	|------------------------------------	|
| 0  	| amplitude                          	|
| 1  	| beyond1std                         	|
| 2  	| flux_percentile_ratio_mid20        	|
| 3  	| flux_percentile_ratio_mid35        	|
| 4  	| flux_percentile_ratio_mid50        	|
| 5  	| flux_percentile_ratio_mid65        	|
| 6  	| flux_percentile_ratio_mid80        	|
| 7  	| fold2P_slope_10percentile          	|
| 8  	| fold2P_slope_90percentile          	|
| 9  	| freq1_harmonics_amplitude_0        	|
| 10 	| freq1_harmonics_amplitude_1        	|
| 11 	| freq1_harmonics_amplitude_2        	|
| 12 	| freq1_harmonics_amplitude_3        	|
| 13 	| freq1_harmonics_freq_0             	|
| 14 	| freq1_harmonics_rel_phase_1        	|
| 15 	| freq1_harmonics_rel_phase_2        	|
| 16 	| freq1_harmonics_rel_phase_3        	|
| 17 	| freq2_harmonics_amplitude_0        	|
| 18 	| freq2_harmonics_amplitude_1        	|
| 19 	| freq2_harmonics_amplitude_2        	|
| 20 	| freq2_harmonics_amplitude_3        	|
| 21 	| freq2_harmonics_freq_0             	|
| 22 	| freq2_harmonics_rel_phase_1        	|
| 23 	| freq2_harmonics_rel_phase_2        	|
| 24 	| freq2_harmonics_rel_phase_3        	|
| 25 	| freq3_harmonics_amplitude_0        	|
| 26 	| freq3_harmonics_amplitude_1        	|
| 27 	| freq3_harmonics_amplitude_2        	|
| 28 	| freq3_harmonics_amplitude_3        	|
| 29 	| freq3_harmonics_freq_0             	|
| 30 	| freq3_harmonics_rel_phase_1        	|
| 31 	| freq3_harmonics_rel_phase_2        	|
| 32 	| freq3_harmonics_rel_phase_3        	|
| 33 	| freq_amplitude_ratio_21            	|
| 34 	| freq_amplitude_ratio_31            	|
| 35 	| freq_frequency_ratio_21            	|
| 36 	| freq_frequency_ratio_31            	|
| 37 	| freq_signif                        	|
| 38 	| freq_signif_ratio_21               	|
| 39 	| freq_signif_ratio_31               	|
| 40 	| freq_varrat                        	|
| 41 	| freq_y_offset                      	|
| 42 	| linear_trend                       	|
| 43 	| max_slope                          	|
| 44 	| median_absolute_deviation          	|
| 45 	| median_buffer_range_percentage     	|
| 46 	| medperc90_2p_p                     	|
| 47 	| p2p_scatter_2praw                  	|
| 48 	| p2p_scatter_over_mad               	|
| 49 	| p2p_scatter_pfold_over_mad         	|
| 50 	| p2p_ssqr_diff_over_var             	|
| 51 	| percent_amplitude                  	|
| 52 	| percent_difference_flux_percentile 	|
| 53 	| QSO                                	|
| 54 	| non_QSO                            	|
| 55 	| scatter_res_raw                    	|
| 56 	| skew                               	|
| 57 	| small_kurtosis                     	|
| 58 	| std                                	|
| 59 	| stetson_j                          	|
| 60 	| stetson_k                          	|

#### Output featues
| \#    	|      Class       	|
|---------	|---------------	|
| 0       	| Mira          	|
| 1       	| Semireg PV    	|
| 2       	| RV Tauri      	|
| 3       	| Classical Cep 	|
| 4       	| Pop. II Cephe 	|
| 5       	| Multi. Mode C 	|
| 6       	| RR Lyrae, FM  	|
| 7       	| RR Lyrae, FO  	|
| 8       	| RR Lyrae, DM  	|
| 9       	| Delta Scuti   	|
| 10      	| Lambda Bootis 	|
| 11      	| Beta Cephei   	|
| 12      	| Slowly Puls.  	|
| 13      	| Gamma Doradus 	|
| 14      	| Pulsating Be  	|
| 15      	| Per. Var. SG  	|
| 16      	| Chem. Peculia 	|
| 17      	| Wolf-Rayet    	|
| 18      	| T Tauri       	|
| 19      	| Herbig AEgBE  	|
| 20      	| S Doradus     	|
| 21      	| Ellipsoidal   	|
| 22      	| Beta Persei   	|
| 23      	| Beta Lyrae    	|
| 24      	| W Ursae Maj   	|


## References
P. Dubath, L. Rimoldini, M. Süveges, J. Blomme, M. L&oacute;pez, L. Sarro, J. De Ridder, J. Cuypers, L. Guy, I. Lecoeur, et al. Random forest automated supervised classification of hipparcos periodic variable stars. *Monthly Notices of the Royal Astronomical Society*, 414(3):2602–2617, 2011

G. Pojmanski. The all sky automated survey. Catalog of about 3800 variable stars. *Acta Astronomica*, 50:177–190, 2000

J. W. Richards, D. L. Starr, N. R. Butler, J. S. Bloom, J. M. Brewer, A. Crellin- Quick, J. Higgins, R. Kennedy, and M. Rischard. On machine-learned classifica- tion of variable stars with sparse and noisy time-series data. *The Astrophysical Journal*, 733(1):10, 2011

J. W. Richards, D. L. Starr, H. Brink, A. A. Miller, J. S. Bloom, N. R. Butler, J. B. James, J. P. Long, and J. Rice. Active learning to overcome sample selection bias: Application to photometric variable star classification. *The Astrophysical Journal*, 744(2):192, 2012