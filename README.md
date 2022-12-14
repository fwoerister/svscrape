# svscrape
[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![Python 3.6](https://img.shields.io/badge/python-3.6-blue.svg)](https://www.python.org/downloads/release/python-360/)
[![PyPI version](https://badge.fury.io/py/svscrape.svg)](https://badge.fury.io/py/svscrape)

SVWebScraper is a tool to parse information of schools listed on http://schulverzeichnis.eu - a database of all austrian schools.
As this site does not provide means for exporting the data to csv files this webscraper was implemented to do so.

## How to use it?
```
$ svscrape --base-url https://schulverzeichnis.eu/typ/ --type neue-mittelschule --query ?bundesland=wien --csv schools.csv
Start scrapping schools from base url ...
20 schools scrapped from "http://www.schulverzeichnis.eu/typ/neue-mittelschule"
40 schools scrapped from "http://www.schulverzeichnis.eu/typ/neue-mittelschule"
...

$ cat ./schools.csv
NAME;ADRESSE;PLZ;ORT;TEL_NR
Freie Waldorfschule Wien-West ;Seuttergasse 29;1130;Wien;01/1234
Mittelschule des Schulvereins der Dominikanerinnen Wien;Schlossberggasse 17;1130;Wien;01/1234
Neue Mittelschule Wien;Neubaugasse 42;1070;Wien;01/1234
...
```

## Documentation
```
$ svscrape --help
Usage: svscrape [OPTIONS]

Options:
  --csv FILENAME
  --baseurl TEXT
  --type [neue-mittelschule|ahs-mit-nms|hauptschule|sonderschule]
  --query TEXT
  --help                          Show this message and exit.
```

## Installing the Latest Version
```
python -m pip install svscrape
```