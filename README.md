# MPE Load Flow Dashboard

An independent Streamlit tool for exploring PowerFactory load-flow sweep results. It provides interactive plots for wind turbine, point-of-connection and equipment results, optional limit checks, and plotted-data CSV export. It does not run PowerFactory studies.

## Open the app

- [Load Flow Dashboard](https://mpe-load-flow.streamlit.app/)
- [MPE Engineering Tools](https://mpe-engineering-tools.streamlit.app/) — landing page for all three dashboards.

The dashboard and landing page are separate public Streamlit Community Cloud apps.

## Input files

- Upload result CSV files individually or together in a ZIP archive.
- Optionally upload a mapping workbook (.xlsx) to label case tokens and group equipment.
- CSV files must use the PowerFactory result format expected by the parser. A mapping workbook changes labels only; it does not change parsed engineering values.

Uploaded files remain in the current browser session. Do not use client data in public issue reports or examples.

## Run locally

Create the dedicated Conda environment and start the app from this repository directory:

    conda env create -f environment.yml
    conda activate mpe-load-flow
    streamlit run app.py

Run the test suite in this environment with:

    python -m pytest -q

## Review and limitations

The tool analyses supplied CSV values and applies the configured plots and limit checks. Confirm input mapping, units and study assumptions, then have a competent engineer review results before using them in a decision.

## Deployment

Deploy app.py from the main branch of this repository in Streamlit Community Cloud. Dependencies are listed in requirements.txt.
