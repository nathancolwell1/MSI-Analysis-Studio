# MSI Analysis Studio

MSI Analysis Studio is a desktop application for reconstructing, visualizing, and analyzing mass spectrometry imaging (MSI) data. It includes workflows for GFP-guided cell detection, manual ROI drawing, ROI feature extraction, statistical analysis, molecular annotation, clustering, and spatial factor mapping.

Current release: **v6.33**

## Main features

- Import and reconstruct MSI datasets
- Browse detected m/z features and adjust MSI contrast interactively
- Clean and crop MSI images without changing the source data
- Run GFP-guided cell detection or draw manual ROIs
- Display optical microscopy beside the MSI during ROI review
- Extract ROI × m/z feature tables
- Filter background ions with noise ROIs and adjustable signal-to-noise thresholds
- Generate PCA, volcano, heatmap, boxplot, clustering, and spatial-analysis outputs
- Save and reopen analysis projects

## Installation (Windows)

1. Install Python 3.10 or newer.
2. Download or clone this repository.
3. Open PowerShell in the project folder.
4. Create and activate a virtual environment:

```powershell
py -m venv .venv
.\.venv\Scripts\Activate.ps1
```

5. Install the dependencies:

```powershell
py -m pip install --upgrade pip
py -m pip install -r requirements.txt
```

6. Start the application:

```powershell
py msi_analysis_studio_v6_33.py
```

## Optional raw-file conversion

Direct vendor raw-file conversion requires ProteoWizard `msconvert`. The application currently expects the Windows installation path defined by `MSCONVERT_PATH` near the top of the Python file. If ProteoWizard is installed elsewhere, update that path before using raw-file conversion.

## Regression check

Run the built-in core checks with:

```powershell
py msi_analysis_studio_v6_33.py --self-test
```

## Notes

- UMAP support is optional but included in `requirements.txt`.
- Molecular database searches may require an internet connection.
- Large MSI projects can require substantial memory and processing time.

