# Data catalog
Root catalog of external and internal datasets

## Accessing datasets
```python
import intake

# Loading catalog
cat = intake.open_catalog("https://raw.githubusercontent.com/ISSI-CONSTRAIN/catalog/main/catalog.yaml")

# Listing sub-catalogs
list(cat)

# Accessing sub-catalogs and their datasets
ds1 = cat['EUREC4A']['simulations']['DALES']['botany']['dx100m']['nx1536']['timeseries'].to_dask()
ds2 = cat['ISCCP']['ISCCP_BASIC_HGM'].to_dask()
ds3 = cat['MPI_TCO']['surfacemet_wxt_v1'].to_dask()
```
