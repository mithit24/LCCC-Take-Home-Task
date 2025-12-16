# LCCC Take-Home Task

  A Python/Jupyter implementation simulating an hourly electricity market auction for the UK power grid. The model computes market-clearing prices (£/MWh) and optimal dispatch
  schedules (wind, solar, gas) based on demand forecasts, renewable availability, and gas plant economics.

  ## Features

  - **Merit-order dispatch**: Renewables dispatched first at £0/MWh, followed by gas plants in ascending bid order
  - **Pro-rata curtailment**: Proportional scaling when renewable output exceeds demand
  - **Marginal pricing**: Market price set by the last accepted gas bid
  - **Comprehensive analysis**: Hourly dispatch breakdowns, price dynamics, and supply mix visualizations

  ## How to Run

  **Prerequisites**: Python 3.7+

  1. Install dependencies:
     ```bash
     pip install numpy pandas matplotlib openpyxl

  2. Ensure data 2.xlsx is in the project directory
  3. Open and run LCCCtask.ipynb in Jupyter Notebook/Lab

  Output

  The notebook generates:
  - Hourly electricity prices (£/MWh)
  - Dispatch schedules for each generation technology
  - Unserved demand tracking
  - Visualizations:
    - Dispatch by technology (area plot)
    - Supply mix as % of demand
    - Hourly price dynamics

  Implementation Notes

  - Renewables: Wind and solar dispatched at £0/MWh; proportional curtailment applied when total renewable output exceeds demand
  - Gas plants: Dispatched in ascending bid order based on fuel costs and efficiency; market price set by marginal accepted bid
  - Unserved demand: Recorded when total available supply cannot meet demand
