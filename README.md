# COVID_moonshot_data_clean
This repository contains comp chem/ML-ready versions of the data in
https://github.com/asapdiscovery/COVID_moonshot_submissions. This data has all been
downloaded from the COVID Moonshot CDD Vault.

The IC50 measurements in this repository were measured using the fluorescence inhibition
assay described in
> Melissa L. Boby,  Daren Fearon, Matteo Ferla, Mihajlo Filep, Lizbé Koekemoer, 
Matthew C. Robinson, The COVID Moonshot Consortium, John D. Chodera,  Alpha A Lee, 
Nir London, Annette von Delft, Frank von Delft. “Open Science Discovery of Potent 
Non-Covalent SARS-CoV-2 Main Protease Inhibitors.” bioRxiv, September 06, 2023.
[https://www.biorxiv.org/content/10.1101/2020.10.29.339317v5](https://www.biorxiv.org/content/10.1101/2020.10.29.339317v5).

On `suspected_SMILES`: Note that many of the enantiopure compounds on this project were
obtained by chiral separation, and thus the compounds are often obtained as a single
enantiomer with unknown absolute stereochemistry. The `suspected_SMILES` column
represents the current understanding of the actual identity of the compound given the current
information, which explains the frequent use of enhanced/relative stereochemistry
representations. 

## Files
* `cdd_noncovalent_dates_2023_10_18_filt.csv`: All noncovalent available
data as of October 10, 2023, filtered to remove data without a noted SMILES string or
IC50 value. Note that some of the entries in this dataset are racemates.
* `cdd_achiral_enantiopure_dates_2023_10_18_filt.csv`: All noncovalent available data as
of October 10, 2023, filtered to contain only achiral and enantiopure molecules.

## Column Headers
A brief explanation of each column present in the CSV files.
* `suspected_SMILES`: SMILES string of the synthesized molecule
* `Canonical_PostEra_ID`: Molecule's canonical name
* `IC50_(µM)`: Experimental IC50 value, in µM units. Unless otherwise noted in the file
description, these values are semi-quantitative, meaning that some values may have been
outside the range of the assay used. The semi-quantitativeness of a given measurement is
given by the `Semiquant` field
* `IC50_CI_(Lower)_(µM)`: Lower bound of the 95% CI of the experimental IC50 value,
in µM units
* `IC50_CI_(Upper)_(µM)`: Upper bound of the 95% CI of the experimental IC50 value,
in µM units
* `Hill_slope`: Calculated slope of the Hill equation for this measurement
* `CDD_curve_class`: Calculated curve class from CDD for this measurement
* `Semiquant`: Whether the given compound was too strong of a binder to be resolved
("Strong"), too weak of a binder to be resolved ("Weak"), or within the assay range
("Quant")

 
