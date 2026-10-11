READ ME: 

This data set is associated with the following manuscript : 

Title: Neurophysiological evidence for crossmodal person-identity representation in the human left ventral temporal cortex

Authors: Angélique Volfart, Jacques Jonas, Louis Maillard, Sophie Colnat-Coulbois, Bruno Rossion


There are three folders, one for each experiment: Experiment_1 with scalp EEG, Experiment_2 with scalp EEG and Experiment_2 with SEEG.
 
Each experiment folder contains a number of folders, one by participant. In Experiment 2, there are 3 folders for each participant, one by condition: FaceName, FaceOnly and NameOnly. 

--- 1. Scalp EEG data ---

For each participant and condition, there are two files (.mat and .lw5) that can be open in Letswave 5, a free software for EEG data analysis (http://www.nocions.org/letswave/) running on Matlab. 

Prior to this step, scalp EEG data (Biosemi 128 channels, BDF files) from Experiment 1 and Experiment 2 have been pre-processed in the following way:

1. Imported in Letswave 5, which has been used for the subsequent steps
2. Filtered with a low cut-off value of 0.1 Hz and high cut-off value of 100 Hz using a butterworth band-pass filter (order 4)
3. Multi-notch filtered (width 0.5) to remove 50 Hz’s electrical noise on 4 harmonics
4. Downsampled to 256 Hz
5. Segmented in order to include 2 seconds of recording before and after each trial (i.e., 2-s baseline + 2-s fade-in + 60-s sequence + 2-s fade-out + 2-s baseline)
6. Unused channels (external electrodes 5 to 8 and status) were removed from the pool of electrodes
7. Filtered with an ICA to correct for eye movements (3 subjects (P01, P02, P12) in Experiment 1, 6 subjects (S10, S15, S16, S26, S29, S20) in Experiment 2)
8. Noisy electrodes across multiple trials (less than 5% of channels) were linearly interpolated with 3 to 6 pooled neighboring channels
9. Re-referenced to a common average reference
10. Cropped,  the 68-second segments being therefore reduced to the 60-second stimulation sequence (or 15235 bins in total) 
11. Averaged in the time-domain

FFT, SNR transform and computations of statistics have not been performed.

--- 2. SEEG data ---

For each patient and condition, there are two files (.mat and .lw5) that can be open in Letswave 5. 

Prior to this step, sEEG data (Micromed, TRC files) from Experiment 2 have been pre-processed in the following way:

1. Imported in Letswave 5, which has been used for the subsequent steps
2. Low-pass filtered with a cut-off at 30Hz using a butterworth low-pass filter (Order 4)
3. Segmented from 2 seconds after the onset of the sequence until ~61 seconds, so that the number of bins in the sequence allows an exact integer number of cycles of the 0.571 Hz identity-change frequency (30471 bins in total). 
4. Merged by condition into one file 

FFT, SNR transform and computations of statistics have not been performed.

In addition, the locations of each intracerebral channel in the Talairach MNI space are reported in an excel file in each participant's folder. Note that these coordinates were used only for display purposes in the current paper. Anatomical definitions were performed on the individual participant's anatomy.