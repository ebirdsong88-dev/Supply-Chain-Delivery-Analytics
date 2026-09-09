# Raw data — download instructions

The raw dataset is not committed to this repo (see `.gitignore`) — it's ~96MB, too large for a normal GitHub repo without Git LFS.

## Download

1. Go to the [DataCo Smart Supply Chain dataset on Kaggle](https://www.kaggle.com/datasets/shashwatwork/dataco-smart-supply-chain-for-big-data-analysis)
2. Download `DataCoSupplyChainDataset.csv`
3. Place it in this folder (`data/raw/`), or update `DATA_DIR` at the top of the notebook to point wherever you saved it

## Notes

- The file uses **Latin-1 encoding**, not UTF-8 — the notebook already handles this (`encoding="latin1"` in the `pd.read_csv` call), but worth knowing if you work with the raw file outside the notebook
- The cleaned dataset (`DataCo_cleaned.csv`, produced by the notebook) is also excluded from version control for the same size reason — regenerate it by running the notebook end to end
