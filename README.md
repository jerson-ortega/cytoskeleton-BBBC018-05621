# Cytoskeleton F-Actin Morphology Analysis (BBBC018)

**Author:** Jerson Lloyd T. Ortega  
**Student ID / Image Identifier:** 05621-actin  
**Phenotype:** Angular cell edges  
**Actin Filename:** `05621-actin.DIB`  
**DNA Filename:** `05621-DNA.DIB`  
**Image-Field ID:** 05621  
**Dataset Source:** [BBBC018v1 - Broad Bioimage Benchmark Collection](https://data.broadinstitute.org/bbbc/BBBC018/BBBC018_v1_images.zip)

---

## 1. Fiji Methodology
1. **Importing Images:** Opened `05621-actin.DIB` and `05621-DNA.DIB` in Fiji (ImageJ) using the Bio-Formats Importer.
2. **Measurement Configuration:** Configured `Analyze > Set Measurements...` to capture **Area**, **Mean gray value**, and **Shape descriptors** (Circularity, Aspect Ratio, Roundness, Solidity).
3. **Cell Tracing:** Synchronized side-by-side views of the actin and DNA channels to identify five distinct, intact cells with single nuclei.
4. **Data Acquisition:** Traced the outer cell boundaries on the actin image using the **Freehand Selection** tool and saved measurements to [`fiji_results.csv`](https://drive.google.com/file/d/113Qc6_lCvpVTFgMGo5cV-SWF7uhP0qy0/view?usp=drivesdk).

---

## 2. Visualizations & Quantitative Results

### Figure 1: Cell Area vs. Circularity
* [area_vs_circularity.png](https://drive.google.com/file/d/1tn-DKaspEv4ZXr5OqpxMEtMHPDn5HTv0/view?usp=drivesdk)

### Figure 2: Mean Actin Signal Intensity
* [actin_intensity.png](https://drive.google.com/file/d/1You_2XjRjeKNYRdrv0mmh9sMSpdkaGQ4/view?usp=drivesdk)

### Summary Statistics
*Complete R Output Spreadsheet:* [`cell_summary.csv`](https://docs.google.com/spreadsheets/d/1Win3Iz8WuUQreGA5isBp85DZGPuX6foxGuOdZvrd_tg/edit?usp=drivesdk&ouid=116887671459865759793)

| Metric | Sample Size ($n$) | Mean Value | Min | Max | Standard Deviation |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **Cell Area** | 5 | **575.60 px²** | 321.00 | 895.00 | 245.02 |
| **Circularity** | 5 | **0.464** | 0.219 | 0.672 | 0.173 |
| **Aspect Ratio (AR)** | 5 | **1.903** | 1.468 | 2.344 | 0.363 |
| **Mean Actin Fluorescence** | 5 | **494.34 AU** | 419.30 | 613.78 | 76.42 |

---

## 3. Reflection & Discussion

1. **Which specific phenotype did you choose, and what visible features support that choice?**
   * **Phenotype:** Angular cell edges.
   * **Supporting Features:** F-actin fluorescence reveals cells with prominent polygonal corners, straight boundary segments, and sharp edges rather than smooth, round, or circular contours.

2. **Were your five cells mostly round or elongated?**
   * The cells were **mostly elongated and morphologically irregular**. The mean aspect ratio was **1.90** (indicating major axes nearly twice as long as their minor axes), and the mean circularity was **0.464** (substantially below 1.0, reflecting non-circular geometry).

3. **What role do actin microfilaments play in cell shape and movement?**
   * Actin microfilaments assemble into cross-linked cortical networks beneath the plasma membrane to maintain structural integrity and dictate cellular geometry. During cell motility, localized actin polymerization pushes the plasma membrane outward at the leading protrusion, while myosin-mediated contractility pulls the trailing edge.

4. **Why can a single fixed image not be used to calculate cell movement speed?**
   * Fixed fluorescence microscopy captures dead, chemically preserved cells at a single static point in time. Velocity calculations require tracking displacement over temporal intervals which can only be measured using continuous live-cell time-lapse imaging.

---

## 4. Data Citation & Credit
This analysis utilizes image dataset **BBBC018v1** from the [Broad Bioimage Benchmark Collection](https://bbbc.broadinstitute.org/BBBC018) (Ljosa et al., *Nature Methods*, 2012). Images are licensed under [CC BY-NC-SA 3.0](https://creativecommons.org/licenses/by-nc-sa/3.0/).
