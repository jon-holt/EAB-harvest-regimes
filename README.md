# EAB-harvest-regimes

The code in this repository corresponds to the paper, "Emerald Ash Borer Intensifies Harvest Regimes on Private Land".

## Data collection

All data were obtained from public resoures. The data were filtered and merged as described in the manuscript.

FIA data were downloaded using the `rFIA` package.
ACS data were downloaded using the `tidycensus` package. 
PRISM data were downloaded using the `prism` package. 
APHIS data were obtained from the USDA APHIS website. 

The merged dataset is provided in the `data` folder.

## Covariate matching

Run the code in `matching.Rmd` to match the data using the Genetic Matching algorithm. 

## Regression analysis

To infer the effect of EAB on harvest intensity and probability, run the zero-inflated beta regressions using Models 1-3. Models 1-3 differ in their treatment of the response variable: 

In Model 1, we consider ash species only.

In Model 2, we consider non-ash species only. 

In Model 3, we consider ash expressed as a fraction of total harvest. 

## Harvest diameter

Run the code in `diameter.Rmd` to compare the diameters of harvested trees in EAB and non-EAB counties. 