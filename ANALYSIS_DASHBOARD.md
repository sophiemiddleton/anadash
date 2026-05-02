# Mu2e Reference Analysis Dashboard

> Interactive analysis results and optimization plots for MDS signal samples

---

## 📊 Analysis Overview

This dashboard provides comprehensive results from the Mu2e reference analysis workflow using SAM dataset discovery and pyCount optimization.

### Dataset Information
- **SAM Definition**: `ensembleMDS3c` (configurable)
- **Analysis Date**: See analysis timestamp in results
- **Signal Polarities**: Minus and Plus
- **File Location**: Disk (configurable)
- **Parallel Jobs**: 8-16 (configurable)

---

## 📈 Key Results

### Cut Statistics (`cut_stats.csv`)
| Metric | Value | Description |
|--------|-------|-------------|
| Total Events | - | Starting event count |
| After Cuts | - | Events passing selection |
| Efficiency | - | Selection efficiency |
| Background Rejection | - | Background suppression factor |

*Note: Load `cut_stats.csv` for detailed statistics with signal/background breakdown*

### Output Files Generated

#### Optimization Plots
- **`*_selection.pdf`**: Cut optimization plots showing efficiency vs background for various selection criteria
- Multiple plots showing momentum, time, and likelihood optimizations
- Available as individual plots for detailed analysis

#### Run Count Plots (from 1D/2D analysis)
- **`1D_Mom.pdf`**: 1D momentum distribution plot
- **`1D_Time.pdf`**: 1D time distribution plot
- **`2D_Time.pdf`**: 2D combined time plot
- Shows event distributions with and without selections

---

## 🔍 Analysis Steps

### 1. Dataset Discovery (SAM Integration)
```
Discover datasets via pyutils.Processor
↓
Create temporary filelist from SAM query
↓
Optionally limit to subset (--max-files N)
```

### 2. Analysis Pipeline
```
For each polarity (minus, plus):
  ├── Load event data from filelist
  ├── Apply preselection cuts
  ├── Optimize selection criteria
  ├── Generate cut statistics (CSV)
  └── Create visualization plots (PDF)
```

### 3. Optimization Output
```
Cut optimization results
├── Efficiency curves
├── Background rejection plots
└── Combined momentum/time plots
```

---

## 📁 Output Directory Structure

```
/exp/mu2e/app/users/sophie/newOffline/RefAna/pyCount/
├── cut_stats.csv                    # Cut statistics table
├── 1D_Mom.pdf                       # 1D momentum plot
├── 1D_Time.pdf                      # 1D time plot
├── 2D_Time.pdf                      # 2D time plot
├── *_selection.pdf                  # Optimization plots (multiple)
├── analysis_dashboard.html          # Interactive web dashboard
└── anadash/
    ├── ANALYSIS_DASHBOARD.md        # This file
    └── analysis_dashboard.html      # HTML dashboard
```

---

## 🚀 Quick Start

### Run Full Analysis
```bash
cd /exp/mu2e/app/users/sophie/newOffline/RefAna/pyCount
./run_analysis.sh --defname ensembleMDS3c --jobs 8
```

### Test with Subset
```bash
./run_analysis.sh --defname ensembleMDS3c --max-files 50 --jobs 8
```

### Interactive Dashboard
Open `analysis_dashboard.html` in a web browser to:
- View cut statistics in an interactive table
- Browse optimization plots
- Explore feature distributions
- Analyze ML classification results

---

## 📊 Detailed Analysis Sections

### Signal Efficiency Region
Shows selection criteria optimized for signal efficiency while maintaining background rejection. Key metrics:
- Signal efficiency: Target 70-90%
- Background rejection: >99%
- Signal purity: Variable based on selection

### Background Suppression
Discusses plot patterns showing:
- Cerium contamination removal (CE plot in `*_selection.pdf`)
- DIO background suppression
- Cosmic ray rejection

### 2D Optimization
Combined plots showing:
- Momentum vs Time correlations
- Efficiency contours
- Optimal selection region boundaries

---

## 🔧 Configuration Options

### Dataset Selection
```bash
--defname DATASET       # SAM definition (default: ensembleMDS3c)
--location LOCATION     # File source: disk/tape/scratch/nersc (default: disk)
```

### Processing Options
```bash
--jobs N                # Parallel jobs (default: 8)
--max-files N           # Limit file count (default: all)
```

### Output Options
```bash
--quiet                 # Suppress colored output
```

---

## 📋 Analysis Metadata

### Process Parameters
- **Environment**: Mu2e CVN cluster environment
- **Python Version**: 3.12+
- **Key Libraries**: hist, boost_histogram, numpy, pandas, matplotlib

### Expected Runtime
- Small subset (10 files): ~5-10 minutes
- Full ensemble (500 files): ~1-2 hours (depending on parallel jobs)

### Quality Checks
- ✓ SAM dataset validation
- ✓ Filelist generation verification
- ✓ Process output file checking
- ✓ Plot generation validation

---

## 📖 Documentation

### Related Files
- **QUICKSTART.md**: Quick reference guide for common tasks
- **AUTOMATION.md**: Detailed automation workflow documentation
- **analysis_dashboard.html**: Interactive web-based results viewer

### Data Files
- **cut_stats.csv**: Detailed cut-by-cut statistics (CSV format)
- **filelist_*.txt**: Temporary file listings (auto-cleaned)

---

## ✨ Features

### Interactive Dashboard (HTML)
- **Cut Statistics Table**: Searchable, sortable CSV data
- **Plot Gallery**: Browse all optimization and analysis plots
- **Feature Analysis**: 8-plot gallery showing feature distributions
- **ML Analysis**: ROC curves, feature importance, score distributions
- **Responsive Design**: Works on desktop and tablet

### Command-Line Automation
- **SAM Dataset Discovery**: Automatic file list generation
- **Parallel Processing**: Configurable job count
- **File Subsetting**: Test with limited file count
- **Environment Management**: Automatic Mu2e environment activation

---

## 🎯 Next Steps

1. **Review Results**
   ```bash
   # Check cut statistics
   cat cut_stats.csv
   
   # View optimization plots
   open 1D_Mom.pdf
   open *_selection.pdf
   ```

2. **Analyze Performance**
   - Compare efficiency across different cuts
   - Evaluate background rejection effectiveness
   - Check signal purity

3. **Fine-tune Selection**
   - If efficiency too low: relax cuts in `process.py`
   - If background too high: tighten cuts
   - Consider 2D selection optimization

4. **Generate Final Results**
   - Full ensemble analysis with optimal parameters
   - Save configuration for reproducibility
   - Document final selection criteria

---

## 📞 Support

For issues or questions:
1. Check QUICKSTART.md for common tasks
2. Review AUTOMATION.md for detailed workflows
3. Examine cut_stats.csv for detailed statistics
4. Open analysis_dashboard.html for interactive exploration

---

**Last Updated**: 2026-05-02  
**Dashboard Version**: 2.0  
**Status**: ✓ Active and Ready
