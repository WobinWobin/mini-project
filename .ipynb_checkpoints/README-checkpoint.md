# ACCeSs@AIM Lab Mini Project - Ng and San Diego

## Parkinson's Disease Detection

### Context
Parkinson’s Disease (PD) is a neurodegenerative disorder characterized by abnormalities in motor and non-motor systems. The common method for diagnosis is based on symptoms such as tremors, depression, and sleep abnormalities. Furthermore, aberrations in speech and vocal qualities are used as indicators of PD. This project focuses on extracting vocal features such as pitch, frequency variation, and amplitude variation, and using it to determine if an individual has Parkinson’s.

---

### Basic Goal: Process Data and Exploratory Data Analysis
1. **Collect audio files** ([Source](https://pmc.ncbi.nlm.nih.gov/articles/PMC5628839/#sec003))
2. **Process audio files** (remove noise from audio files) 
3. **Feature Extraction**
    * Utilize `parselmouth` and/or `speechbrain` 
    * Get features from audio files, potentially including but not limited to: 
        * **F0 / Pitch features:** MDVP: Fo, Fhi, Flo
        * **Jitter (frequency variation):** MDVP:Jitter(%), Jitter(Abs), RAP, PPQ, DDP
        * **Shimmer (amplitude variation):** MDVP: Shimmer, APQ3, APQ5, DDA
        * **Noise/periodicity:** NHR, HNR
        * **Nonlinear / complexity features:** RPDE, DFA, spread1/2, D2, PPE
4. **Perform EDA** (boxplot for healthy vs Parkinson’s) and **Logistic Regression**

---

### Intermediate Goal: Apply Signal Analysis
1. **Perform FFT** ([Source](https://www.sciencedirect.com/science/article/pii/S0003682X25006899#s0025)) and **Wavelet Transformation** 2. **Get Spectral Features:**
    * Spectral Centroid
    * Mel-Frequency Cepstral Coefficients (MFCCs)
    * Spectral bandwidth
    * Spectral contrast ([Source](https://www.mdpi.com/2306-5354/12/10/1052))
3. **Perform EDA** (boxplot for healthy vs Parkinson’s) 
4. **Make a dataframe:** healthy vs Parkinson’s 

---

### Advanced Goal: Run Machine Learning Models
1. **Feed the dataframe into the models**
    * Perform **KNN**
    * Perform **Random Forest**
    * **Logistic Regression** 2. **Find Feature importance** 3. **Compare results**