# Bayes Hack 2016

### Department of Transportation Prompt #3
_How can data optimize emergency services?_

## Prompt

In 2014 there were more than 6 million traffic crashes in the United States, resulting in 32,675 deaths and 2.3 million injuries. Based on incident and traffic conditions, emergency responders have a number of options for transportation (including helicopter ambulance transport in lieu of ground ambulance). There aren't standardized methods or technologies designed for emergency medical services personnel to predict and optimize transport times by selecting the right response to every incident.

Can rich EMS response data coupled with incident state—including weather conditions, road and traffic conditions, and hospital locations—be used to develop a real-time tool for paramedics and dispatchers?

## Datasets

Two datasets that may come in handy for this prompt are the traffic-fatalities dataset from **FARS** (the Fatality Analysis Reporting System) and the EMS usage dataset from **NEMSIS** (the National EMS Information System):

**TODO: Clean up the rest of this section.**

### FARS traffic fatalities dataset

- Can be queried from http://www-fars.nhtsa.dot.gov//QueryTool/QuerySection/SelectYear.aspx
- Or see the full data dump for 2014 (in TSV form) in `/data`
- See `fars-exploration.ipynb` for brief exploration of the data dump

### NEMSIS (National EMS Information System)

- 4GB data dump from 2014 (in TSV form) available at https://drive.google.com/open?id=0B72-YWd6iouWaU4tTjFrd2FtTk0
- Coming soon: Makefile to automatically download and extract the data dump.

## In This Repo

* `data/`
  * `nemsis/` – this is where the Makefile will download the national NEMSIS 2014 data dump.
  * `nemsis-illinois/` – this is where the Makefile will download the Illinois NEMSIS 2014 data dump.
  * `fatalities-2014-allfields.tsv` – a dump of all 2014 crash/driver/occupant/vehicle/pre-crash data fields from FARS, in TSV format.
  * `fatalities-fieldnames.tsv` – a mapping of field-codes to descriptive field names for the FARS dataset.
  * `fatalities-codes.txt` – a raw text dump of the meanings of all relevant codes for `fatalities-2014-allfields.tsv`.
* `analysis/`
  * `fars-exploration.ipynb` – iPython (Jupyter) basic exploration notebook for the FARS dataset.
* `Makefile` – scripts to download the NEMSIS dataset.

## Resources

- The American Trauma Society hosts a [comprehensive index of trauma centers](http://www.amtrauma.org/?page=FindTraumaCenter) in the United States that incorporates service information.
- The National Highway Traffic Safety Administration's National Center for Statistics and Analysis [open data portal](http://www.nhtsa.gov/NCSA) with troves of high-level statistics. They also run the [Fatality Analysis Reporting System](http://www-fars.nhtsa.dot.gov//QueryTool/QuerySection/SelectYear.aspx), which can be queried year-by-year for individual traffic accident conditions and outcomes _([see the README section on FARS data](#fars-traffic-fatalities))_.
