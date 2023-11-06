# COVID_moonshot_data_clean
This repository contains cleaned versions of the data in
https://github.com/asapdiscovery/COVID_moonshot_submissions.

## Files
`cdd_achiral_enantiopure_dates_2023_10_18_filt.csv`: All available data as of October
10, 2023, filtered to contain only achiral and enantiopure molecules.

## Column Headers
A brief explanation of each column present in the CSV files.
* `Canonical_PostEra_ID`: Molecule's canonical name
* `suspected_SMILES`: SMILES string of the synthesized molecule
* `IC50_(µM)`: Experimental IC50 value, in µM units
* `IC50_CI_(Lower)_(µM)`: Lower bound of the 95% CI of the experimental IC50 value,
in µM units
* `IC50_CI_(Upper)_(µM)`: Upper bound of the 95% CI of the experimental IC50 value,
in µM units
* `Hill_slope`: Calculated slope of the Hill equation for this measurement
* `Curve_class`: Calculated curve class for this measurement
* `In_range`: Whether the given measurement was above, below, or within the assay range
