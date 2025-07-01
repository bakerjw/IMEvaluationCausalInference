# Ground Motion Intensity Measure Evaluation Using Causal Inference

This repository contains research code for evaluating the effectiveness of ground motion intensity measures using efficiency, sufficiency, and causal inference methods.

## Publication

This code accompanies the following paper:

Burton, H. V., and Baker, J. W. (2023). "Evaluating the effectiveness of ground motion intensity measures through the lens of causal inference." *Earthquake Engineering & Structural Dynamics*, 52(15), 4842–4864. http://doi.org/10.1002/eqe.3983

## Authors

- Henry Burton (UCLA)
- Jack Baker (Stanford University)

## Overview

The codebase implements three complementary approaches for evaluating ground motion intensity measures:

1. **Efficiency-based evaluation** - Assesses how well intensity measures predict structural response
2. **Sufficiency-based evaluation** - Tests whether intensity measures capture all relevant ground motion characteristics
3. **Causal inference analysis** - Uses causal inference methods to evaluate intensity measure effectiveness

## Requirements

### MATLAB
- Base MATLAB installation

### R
- `randomForest` package
- `tictoc` package  
- `EnvStats` package
- `rmarkdown` package

## Usage

### Data Preparation
First, extract the data files:
```bash
unzip Data.zip
```

### MATLAB Analysis
Run the MATLAB scripts in the following order:
```matlab
% Convert raw CSV data to MATLAB .mat files
run('GenerateMATFiles.m')

% Perform efficiency-based evaluation
run('EfficiencyEvaluation.m')

% Perform sufficiency-based evaluation
run('SufficiencyEvaluation.m')
```

### R Analysis
Generate the causal inference analysis:
```r
# Render the R Markdown document
rmarkdown::render('BaselineCausalInference.Rmd')
```

## Data Structure

- `Data/Raw/` - Original CSV files with ground motion data and structural responses
- `Data/Processed/matFiles/` - Processed MATLAB data files
- `Results/` - Analysis results organized by method (Efficiency, Sufficiency, CausalInference)

## License

This research code is provided for academic and research purposes.
