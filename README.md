# COVID_moonshot_data_clean
This repository contains cleaned versions of the data in
https://github.com/asapdiscovery/COVID_moonshot_submissions. This data has all been
downloaded from the COVID Moonshot CDD Vault.

On `suspected_SMILES`: Note that many of the enantiopure compounds on this project were
obtained by chiral separation, and thus the compounds are often obtained as a single
enantiomer with unknown absolute stereochemistry. The `suspected_SMILES` column
represents the understanding of the actual identity of the compound given the current
information, which explains the frequent use of enhanced/relative stereochemistry
representations. Keep in mind that the `suspected_SMILES` is often not the same as the
`registration_SMILES`, since compounds must be registered as a real (non-relatively
defined) compound on this project.

## Files
* `cdd_noncovalent_dates_2023_10_18_unfiltered_clean.csv`: All noncovalent available
data as of October 10, 2023, cleaned to remove data without a noted SMILES string or
IC50 value
* `cdd_achiral_enantiopure_dates_2023_10_18_filt.csv`: All noncovalent available data as
of October 10, 2023, filtered to contain only achiral and enantiopure molecules.

## Column Headers
A brief explanation of each column present in the CSV files.
* `Canonical_PostEra_ID`: Molecule's canonical name
* `suspected_SMILES`: SMILES string of the synthesized molecule
* `IC50_(µM)`: Experimental IC50 value, in µM units. Unless otherwise noted in the file
description, these values are semi-quantitative, meaning that some values may have been
outside the range of the assay used. The semi-quantitativeness of a given measurement is
given by the `Semiquant` field
* `IC50_CI_(Lower)_(µM)`: Lower bound of the 95% CI of the experimental IC50 value,
in µM units
* `IC50_CI_(Upper)_(µM)`: Upper bound of the 95% CI of the experimental IC50 value,
in µM units
* `Hill_slope`: Calculated slope of the Hill equation for this measurement
* `Curve_class`: Calculated curve class for this measurement
* `Semiquant`: Whether the given compound was too strong of a binder to be resolved
("Strong"), too weak of a binder to be resolved ("Weak"), or within the assay range
("Quant")
