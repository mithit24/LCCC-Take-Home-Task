# LCCC Take-Home Task

This repo contains a Python/Jupyter implementation of an hourly electricity market auction.
It computes hourly prices (£/MWh) and dispatch (wind, solar, gas) based on demand, renewable
load factors, and gas bid costs derived from fuel prices and efficiencies.

## How to run
1. Install dependencies:
   pip install numpy pandas matplotlib openpyxl
2. Put `data 2.xlsx` in the same folder.
3. Open and run `LCCCtask.ipynb`.

## Notes
- Renewables dispatched first at £0/MWh; proportional curtailment if renewables exceed demand.
- Gas plants dispatched in ascending bid order; price set by marginal accepted bid.
- Unserved demand recorded if supply is insufficient.
