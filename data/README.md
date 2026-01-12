# Data Directory README

This folder contains **instructions and metadata for obtaining and preparing the external datasets** used in this project.  
**Raw catalogs are not included** .

---

## Required Datasets

You will need to manually download the following data products:

### 1. **SDSS DR7 Value-Added Catalogs (MPA-JHU)**
- Website: http://www.mpa-garching.mpg.de/SDSS/DR7/
- Key files:
  - `gal_info_dr7_v5_2.fit.gz` (galaxy info)
  - `totlgm_dr7_v5_2.fit.gz` (stellar mass)
  - `gal_totsfr_dr7_v5_2.fits.gz` (star formation rate)
  - `gal_fnal_dr7_v5_2.fit.gz` (CMODEL)
  - `gal_line_dr7_v5_2.fit.gz` (spectroscopic data)
  - `gal_indx_dr7_v5_2.fit.gz` (D4000)

### 2. **Best & Heckman (2012) RLAGN Table**
- Source: [CDS Vizier J/MNRAS/421/1569](https://cdsarc.cds.unistra.fr/ftp/J/MNRAS/421/1569/table1.dat)
- File: `table1.dat`

### 3. **Janssen et al. (2012) Derived Data**
- Paper: https://arxiv.org/abs/1206.0578
- Use features and logic described in the paper.

### 4. **LoTSS DR2 AGN Value-Added Catalogue**
- Source: [LoTSS DR2](https://lofar-surveys.org/releases.html)  
- File: [`agn-v1.1.fits`](https://lofar-surveys.org/public/DR2/AGN_selection/agn-v1.1.fits) (or latest AGN value-added catalogue)
- Reference: Hardcastle et al. 2023, A&A, 678, 151

---

## Data Preparation

- **Download and extract** all catalog files above into this `data/` folder.
- No pre-processing is needed; the notebooks will handle format conversion and merging.
- For sample code on how to read these files with `astropy.table` or `pandas`, see code comments in each notebook.

---

