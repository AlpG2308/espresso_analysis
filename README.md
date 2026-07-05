# Espresso Analysis

A small applied science project exploring espresso brewing dynamics using my own logged shots on a DeLonghi La Specialista Arte (9-bar pump, PID boiler, conical burr grinder, manual tamp).

## What this is

Five of my own brewed and tasted shots from an orthogonal array (more or less, some issues kept me from setting the expirement up properly), analyzed with:

1. A **real Buckingham Π dimensional analysis** (dimensional matrix + null
   space, computed with `sympy`, not asserted by hand).
2. Taste profiles plotted in the resulting **dimensionless Π-space**
   (brew ratio vs. a flow/pressure number), plus a per-shot sensory radar.
3. An explicit **causal DAG** of the brewing mechanism (grind/dose/tamp/
   pressure → time/yield → crema/acidity/body)
4. The v1 geometry/oracle machinery, it's a reward-weighted diffusion over Π-space similarity.
5. A **synthetic testbed**




## Files

- `lcf_espresso_oracle.ipynb`


## Running it yourself

`lcf_espresso_oracle.ipynb` directly in Jupyter/JupyterLab and
run all cells.

## Where this is weakest, and what would fix it (Section 8 in the notebook)

1. No interventional design need to hold variables fixed and sweep one
   at a time to make the DAG's edges actually estimatable.
3. Grinder dial isn't calibrated to a physical particle size needed to -> Calibrate. Rather hard without proper scientific equipment.
4. n = 5 is too small for the coherence geometry (Section 5)