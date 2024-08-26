# H2Combustion_BO-POL

Wiberg/Mayer Bond Indices and Polarizabilities for the Hydrogen Combustion Dataset IRC's computed with wb97x-v/cc-pVTZ

## Data Format

The data is stored in compressed and zipped NumPy archives and contains the total DFT energy (E), Mulliken gross population (MQ), NBO Natural population (NQ), NAO Wiberg bond index (WBI), NAO Mayer bond index (MBI), NAO Mulliken overlap population (MOP), dipole polarizability tensor (ALPHA). The first dimension of each array corresponds to the IRC image (`data['R'][0]` contains the coordinates `(n_atoms, 3)` for the first frame along the IRC).

```python
>>> import numpy as np
>>> data = np.load('H2COMBUSTION-BO-POL-IRC/01_irc.npz', allow_pickle=True)
>>> [k for k in data.keys()]
['R', 'Z', 'N', 'E', 'CONV', 'TIME', 'MQ', 'NQ', 'WBI', 'MBI', 'MOP', 'ALPHA']
```

See the Jupyter notebook, [plots.ipynb](https://github.com/THGLab/H2Combustion_BO-POL/blob/main/plots.ipynb), for figures.
