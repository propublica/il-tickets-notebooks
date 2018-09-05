# Chicago Tickets Example Notebooks

ProPublica Illinois and WBEZ [cleaned and released](https://www.propublica.org/datastore/dataset/chicago-parking-ticket-data) the records for all parking and vehicle compliance tickets in Chicago from Jan. 1, 2007 to May 14, 2018.

This repository contains a sample of that data and is intended to be a community resource for those who want to work with this data by providing notebooks with analysis and visualization.

To contribute, fork this repository, add a Jupyter notebook (Python and R preferred), and submit a pull request.

See the notebook entitled [start-here.ipynb](start_here.ipynb).

Want to learn more about Jupyter notebooks? Ben Welsh's [First Python Notebook](http://www.firstpythonnotebook.org/) is a great introduction.

# Requirements

* Python 3.5+ (`brew install python` on OS X)

# Install

Some form of [virtual environment](https://docs.python-guide.org/dev/virtualenvs/) is recommended.

```
pip install -r requirements.txt
```

# Run

```
jupyter notebook
```

# Contributing

* Fork this repository.
* Add a descriptively named notebook file, e.g. `western-ave-analysis.ipynb` and add your analysis and visualization.
* Add a link to the "Available notebooks" list in `README.md`.
* Create a pull request.

# Available notebooks

* [start-here.ipynb](start-here.ipynb): Loads the data, nothing more.
* _Add yours!_

# Data warning

The data provided is a 50,000 row sample from the year 2015. The sample size was picked for convenience, not scientifically. We are not certain the results are truly random. This dataset should not be used for any published analysis, nor shall ProPublica be held liable for any use of this data. If you intend to publish or make decisions based on the notebooks in this repository, download and use [the full dataset](https://www.propublica.org/datastore/dataset/chicago-parking-ticket-data) published by ProPublica Illinois.
