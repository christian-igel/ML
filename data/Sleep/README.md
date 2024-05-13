# Sleep Staging
Sleep is one of the most fundamental physiological processes, and abnormal sleeping patterns are associated with poor health. They may, for example, indicate  brain- \& heart diseases, obesity and diabetes.
During sleep our brain goes through a series of changes between different sleep stages, which are characterized by specific brain and body activity patterns.

*Sleep staging* refers to the process of mapping these transitions  over a  night of sleep.
This is of fundamental importance in sleep medicine, because the sleep patterns combined with other variables provide the basis for diagnosing many sleep related disorders (Kales and Rechtschaffen 1968, C. Iber and AASM 2007}.

The stages can be determined by measuring the neuronal activity in the cerebral cortex (via electroencephalography, EEG), eye movements (via electrooculography, EOG), and/or the activity of facial muscles (via electromyography, EMG) in a  polysomnography (PSG) study. The classification into stages is done manually. This is a difficult and time-consuming process, in which expert clinicians inspect and segment the typically 8-24 hours long multi-channel signals. 
Contiguous, fixed-length intervals of 30 seconds are considered, and each of these segments is  classified individually.
Algorithmic sleep staging aims at automating this process.
The state-of-the-art 
in algorithmic sleep staging is marked by deep neural networks, which 
can be highly accurate and robust, even compared to human performance, see the recent work by 
Perslev et al. (2019, 2021)
and references therein.

This assignment considers algorithmic sleep staging.
The data is based on a single EEG channel from the  Sleep-EDF-15 data set ()Kemp et al. 2000).
The input is given by an intermediate representation from the U-Time neural network architecture (Perslev et al. 2019), the targets are sleep stages.
We created a training and test set, the inputs and the corresponding labels can be found in
`X_train.csv` and `X_test.csv` and `y_train.csv` and `y_test.csv`, respectively

## References
A. L. Goldberger, L. A. N. Amaral, L. Glass, J. M. Hausdorff, P. Ch. Ivanov, R. G.
Mark, J. E. Mietus, G. B. Moody, C.-K. Peng, and H. E. Stanley. PhysioBank,
PhysioToolkit, and PhysioNet: Components of a new research resource for
complex physiologic signals. *Circulation*, 101(23):e215–e220, 2000

C. Iber and AASM. *The AASM manual for the scoring of sleep and associated
events: rules, terminology and technical specifications*. American Academy of
Sleep Medicine, Westchester, I. L., 2007

A. Kales and A. Rechtschaffen. *A manual of standardized terminology, techniques
and scoring system for sleep stages of human subjects*. Allan Rechtschaffen and
Anthony Kales, editors. U. S. National Institute of Neurological Diseases and
Blindness, Neurological Information Network Bethesda, Md, 1968

B. Kemp, A. H. Zwinderman, B. Tuk, H. A. C. Kamphuisen, and J. J. L. Oberye.
Analysis of a sleep-dependent neuronal feedback loop: the slow-wave microcontinuity of the EEG. *IEEE Transactions on Biomedical Engineering*, 47(9):
1185–1194, 2000

M. Perslev, M. Hejselbak Jensen, S. Darkner, P. J. Jennum, and C. Igel. U-time:
A fully convolutional network for time series segmentation applied to sleep
staging. In *Advances in Neural Information Processing Systems* (NeurIPS),
2019

M. Perslev, S. Darkner, L. Kempfner, M. Nikolic, P. J.  Jennum, and C. Igel. [U-Sleep: Resilient High-Frequency Sleep Staging](https://doi.org/10.1038/s41746-021-00440-5). *npj Digital Medicine* 4, 2021
