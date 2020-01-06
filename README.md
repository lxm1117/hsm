![HSM Banner Image](misc/symbol_name.large.png)

# hsm - Biophysical prediction of protein-peptide interactions and signaling networks using machine learning. 

This repository implements the hierarchical statistical mechanical (HSM) model described in the paper [Biophysical prediction of protein-peptide interactions and signaling networks using machine learning.](nature.com) 

An **associated website** is available at [proteinpeptide.io](proteinpeptide.io). The website is built to facilitate interactions with results from the model including: (1) specific domain-peptide and protein-protein predictions, (2) the resulting networks, and (3) structures colored using the inferred energy functions from the model. Code for the website is available via the parallel repo: [aqlaboratory/hsm-web](https://github.com/aqlaboratory/hsm-web).

This file documents how this package might be [used](#usage), the [location of associated data](#data), and [other metadata](#reference). 

## Usage

The model was implemented in Python (>= 3.5) primarily using TensorFlow (>= 1.4). Additional package requirements are listed in [requirements.txt](requirements.txt). To work with this repository, we recommend downloading pre-processed data available at [doi:](figshare.com) into "data/". Alternatively, it is possible to either re-process raw data ([doi:](figshare.com)) or include new data. The folder contains two major directories: `train/` and `predict/`. Each directory is accompanied by a `README.md` file detailing usage. 

To train / re-train new models, use the `train.py` script in `train/`. To make predictions using a model, use one of two scripts, `predict_domains.py` and `predict_proteins.py`, for predicting either domain-peptide interactions or protein-protein interactions. Scripts are designed with a CLI and should be used from the command line: 

```bash
python [SCRIPT] [OPTIONS]
```

Options for any script may be listed using the `-h/--help` flag. 

Pre-processed / pre-trained data and models may be downloaded from [figshare/doi:](figshare.com) and should be unpacked at `data/` in this directory. This directory may also be used as an example of how to structure input and output files / directories.

An alternative use case would be to train / re-train a new model in the `train/` code and make new predictions using the `predict/` code. 

## Data

As reported, domain-peptide and protein-protein interactions are available via [figshare/doi:](figshare.com). In addition, we provide pre-processed data for this repository and the website repository, 

- Raw training data: [figshare/doi:](figshare.com). Raw domain-peptide training data used to train the core HSM models. Unpack to `data/` in this directory.
- Website data: [figshare/doi:](figshare.com). Data supporting the website at [proteinpeptide.io](proteinpeptide.io)

The data used to the train the model is also provided at a separate data repository: [figshare/doi:](figshare.com). 

## Reference
Please reference the associated publication:

Cunningham, J.M., Koytiger, G., Sorger, P.K., & AlQuraishi, M. "Biophysical prediction of protein-peptide interactions and signaling networks using machine learning." *Nature Methods* (2020). [doi:](https://doi.org/). ([citation.bib](https://raw.githubusercontent.com/aqlaboratory/hsm/misc/citation.bib))

See also, a **website** at [proteinpeptide.io](proteinpeptide.io) for exploring the associated analyses (code: [aqlaboratory/hsm-web](https://github.com/aqlaboratory/hsm-web)). 

## Funding

This work was supported by the following sources:

| **Funder** | **Grant number** |
| ---------- | ---------------- |
| NIH | U54-CA225088 |
| NIH | P50-GM107618 |
| DARPA / DOD | W911NF-14-1-0397 |

## License
This repository is released under an [MIT License](LICENSE)