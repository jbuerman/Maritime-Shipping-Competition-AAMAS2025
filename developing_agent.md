---
layout: page
title: Developing an Agent
permalink: /agentdev/
---

For the competition you will need to implement a `TradingCompany` for the MABLE simulator.
Please have a look at our [(Setup) Guide](https://github.com/jbuerman/Maritime-Shipping-Competition-AAMAS2025/raw/main/files/AAMAS2025_maritime_bidding_competition_guide.pdf){:target="_blank"}, which also includes instructions on the required [resources](https://github.com/jbuerman/Maritime-Shipping-Competition-AAMAS2025/raw/main/files/mable_resources.zip){:target="_blank"}, and the Creating a Trading Company guide in on the [API page](https://mable-doc.netlify.app/tradingagentintroduction){:target="_blank"}.

## Additional Python Packages {#additional-python-packages}

You are allowed to use additional python packages.
However, you can only use those packages and versions approved by us.
Following is a list of packages and their versions which have been approved.
If you would like to add a package to the list, please get in contact with us via [msc.aamas2025@soton.ac.uk](mailto:msc.aamas2025@soton.ac.uk).

### Approved Versions of Additional Package's

## Evaluating Agents {#evaluating-agents}

As described in Section 3.2 of the [(Setup) Guide](https://github.com/jbuerman/Maritime-Shipping-Competition-AAMAS2025/raw/main/files/AAMAS2025_maritime_bidding_competition_guide.pdf){:target="_blank"} each simulator run generates an output file `metrics_competition_<number>_<timestamp>.json` (where number is a random number and the timestamp is generated at the end of the simulation when the metrics are being exported).

The output file are JSON encoded metrics of the simulation run containing the following information:

The outermost structure is a dict with four keys: `company_names`, `company_metrics`, `vessel_metrics` and `global_metrics`.

- `company_names`
  - Matching between an ID identifying a company in the rest of the output and the company's name
- `company_metrics`
  - Overall metrics of the companies (indexed by their ID) summed over all vessels in their fleet.
    - `fuel_consumption`
      - Total amount of consumed fuel
    - `fuel_cost`
      - The cost of the consumed fuel
    - `co2_emissions`
      - The total CO2 emissions from the consumed fuel
    - `vessel_status_ballast`
      - Based on the time vessels are travelling without cargo
    - `vessel_status_laden`
      - Based on the time vessels are travelling with cargo
    - `vessel_status_loading`
      - Based on the time vessels are loading cargo in port
    - `vessel_status_unloading`
      - Based on the time vessels are unloading cargo in port
    - `vessel_status_idle`
      - Based on the time vessels are not performing any of the other operations (ballast, laden, loading and unloading), i.e. the remaining time.
- `vessel_metrics`
  - Same types of metrics as for the overall company but per vessel (indexed by (company ID, vessel ID). Additionally, the entire route the vessel has taken during the simulations.
- `global_metrics`
  - Contains information on auction outcomes and penalties
    - `auction_outcomes`
      - A list with one dict per run auction. Each individual auction dict contains lists of the won contracts per company (indexed by the company IDs). The individual contracts listed contain all information about the trade as well as the payment of the contract and an indicator if the trade was fulfilled by the company.
    - `penalty`
      - The total penalty each company had to pay for unfulfilled contracts (indexed by the company IDs).
