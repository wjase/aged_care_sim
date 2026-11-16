# Aged Care Cost Simulator

A browser-based planning tool for modelling aged care accommodation costs, daily fees, home sale proceeds, investments, and remaining assets over time. It is an illustration, not financial advice.

## Run it

Open `aged-care-simulator.html` in a modern web browser. No build step or installation is required. An internet connection is needed to load Mermaid for the charts.

## Use the simulator

1. Set the daily fees, assets and income, monthly expenses, accommodation settings, and simulation length.
2. Results update when you change an input. Use **Reset to defaults** to restore the starting assumptions.
3. Use **Download results (CSV)** for yearly data, **Download parameters (JSON)** to save inputs, **Upload parameters (JSON)** to load them later, or **Download report (Markdown)** for a detailed report.

Inputs are saved in the browser's local storage. They are local to that browser and device.

## Model notes

- Daily fees are charged for 365 days per year without indexation. The default Higher Every Day Living Fee (EDLF) is $29.80 per day. (Nov 2026)
- The NCCC stops when either its time cap or value cap is reached.
- Retention is calculated as a percentage of the refundable RAD for up to the configured number of years. It is included in outgoing costs and deducted from the refundable RAD balance.
- From the configured house-sale year, the simulator first uses sale proceeds to top up the RAD. After annual fees and retention, it attempts to restore the RAD to the room maximum, using investments from that year onward. If funds are insufficient, fees are prioritised and the RAD may remain below the maximum.
- By default, daily fees are debited from the refundable RAD; any amount not covered by the RAD is funded from investments. Other fee-source options are available.
- The tax, income, and asset assumptions are simplified. Check fee amounts and caps against current legislation and Services Australia figures.

