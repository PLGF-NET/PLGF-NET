# PLGF-NET: Physics-Guided Local-Global Fusion Network

This repository contains the official PyTorch implementation for the paper:  
**"Difficulty-Aware Data Resampling and Selective Physics-Informed Learning for GNSS-R High Wind Speed Retrieval".

##  Repository Status: Structural Preview
The source code currently available in this repository serves as a **structural preview** of the PLGF-NET framework. 

To protect intellectual property while our manuscript is under peer review, the core proprietary algorithm implementations have been temporarily redacted (replaced with `NotImplementedError`). This includes:
- The precise formulations for the Sample Prediction Difficulty (SPD).
- The mask generation mechanism for the Physics-Guided Spatial Attention (PGSA).
- The empirically fitted Geophysical Model Function (GMF) parameters.

**The complete, fully executable source code, along with the pre-trained weights and data processing scripts, will be publicly released immediately upon the acceptance of the paper.**

##  Overview
Accurate global sea surface wind speed retrieval, especially under extreme high wind conditions (> 15 m/s), remains a critical challenge for spaceborne Global Navigation Satellite System Reflectometry (GNSS-R) due to inherent physical limitations such as long-tail data distribution, low signal-to-noise ratio, and scattering signal saturation. To overcome the performance degradation of existing models in these regimes, this study proposes a novel physics-data dual-driven paradigm, instantiated as the Physics-Guided Local-Global Fusion Network (PLGF-NET). A physics-aware Comprehensive Difficulty Score (CDS) is introduced to quantify the intrinsic complexity of Delay-Doppler Maps (DDMs), driving a hierarchical sampling strategy to dynamically mine the scarce features of extreme sea states. To accurately process these complex samples, a Physics-Guided Spatial Attention (PGSA) mechanism translates specular reflection theory into a structural prior mask. This constraint enforces a crucial feature purification process, compelling the network to maintain its focus on the effective scattering window while suppressing peripheral thermal noise. Furthermore, geophysical consistency is ensured through a selective regularization mechanism based on Sample Prediction Difficulty (SPD). Rather than applying uniform constraints to the model, this approach adaptively enforces Geophysical Model Function (GMF) consistency exclusively on high-uncertainty samples, serving as a physical anchor against signal saturation. Extensive evaluations demonstrate that PLGF-NET exhibits state-of-the-art robustness, achieving an overall root mean square error (RMSE) of 1.38 m/s and significantly reducing the high-wind RMSE to 2.40 m/s. This dual-driven framework lays a scalable and physically interpretable foundation for extreme marine environment monitoring.

##  Requirements
- Python 3.8+
- PyTorch >= 1.10.0

##  Citation
If you find our work or this framework useful, please consider citing our paper (BibTeX will be updated upon publication).
