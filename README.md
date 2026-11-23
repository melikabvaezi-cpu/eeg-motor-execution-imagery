# EEG Analysis of Motor Execution and Motor Imagery

An independent computational neuroscience project comparing sensorimotor EEG activity during **actual** (motor execution) and **imagined** (motor imagery) left- and right-hand movements.

**Author:** Melika B. Vaezi, M.S. student in Kinesiology, Texas Tech University

## Question
Do actual and imagined hand movements produce the same pattern of sensorimotor oscillations over the contralateral and ipsilateral hemispheres?

## Data
[PhysioNet EEG Motor Movement/Imagery Dataset](https://physionet.org/content/eegmmidb/1.0.0/) (64-channel EEG, BCI2000). Raw data are not stored in this repository. The notebook downloads them with `mne.datasets.eegbci`.

## Methods
- Preprocessing in MNE-Python: band-pass filtering, epoching around task cues, baseline (rest) period
- Channels: C3, Cz, C4 (sensorimotor cortex)
- Spectral power in the Alpha (8–13 Hz) and Beta (13–30 Hz) bands
- Event-related desynchronization/synchronization (ERD/ERS) relative to rest
- Contralateral vs. ipsilateral comparison for left- and right-hand trials

## Preliminary results
In this single-subject analysis, motor execution showed a clearer contralateral Alpha power decrease than motor imagery, which showed a less consistent hemispheric pattern. These results are exploratory and limited to one participant.

![ERD/ERS figure](figures/erd_ers.png)

## How to run
```bash
pip install -r requirements.txt
jupyter notebook eeg_motor_execution_imagery.ipynb
```

## Tools
Python, MNE, NumPy, Pandas, Matplotlib

## Next steps
- Time-frequency analysis of Alpha and Beta over the trial
- Scalp topographic maps (topomaps)
- More participants, and classification of execution vs. imagery
