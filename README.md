# FoundationModel0

This repositropy mainly collects the essential information of one of the best foundation model in atomistic materials chemistry:

1. What are the MACE-MP-0 models?
https://github.com/ACEsuit/mace?tab=readme-ov-file#pretrained-foundation-models

2. Where are these models?
https://github.com/ACEsuit/mace-mp/releases/tag/mace_mp_0

3. How to use these models?
Install MACE: https://github.com/ACEsuit/mace 

#### Example usage in ASE
```py
from mace.calculators import mace_mp
from ase import build

atoms = build.molecule('H2O')
calc = mace_mp(model="medium", dispersion=False, default_dtype="float32", device='cuda')
atoms.calc = calc
print(atoms.get_potential_energy())
```
