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

# Unofficial data dictionary

* ticket_number: a unique ID for each citation
* issue_date: date and time the ticket was issued
* violation_location: street address where the ticket was issued
* license_plate_number: contains a hash, making it possible to determine whether tickets were issued to the same vehicle, while anonymizing the actual license plate numbers.
* license_plate_state: what state the license plate is from, expressed as a two-letter abbreviation 
* license_plate_type: the vast majority of license plates are for passenger vehicles. But also included are trucks, temporary plates and taxi cabs, among many others.
* zipcode: the ZIP code associated with the vehicle registration
* violation_code: municipal code associated with violation; these have changed slightly over time
* violation_description: name of violation
* unit: This number relates to subcategories within units, such as police precincts or private contractors. A file with a unit crosswalk obtained from the Department of Finance is included in the data download. 
* unit_description: the agency that issued the ticket, typically “CPD” for Chicago Police Department or “DOF” for Department of Finance, which can include subcontractors.
* vehicle_make: vehicle make
* fine_level1_amount: original cost of citation
* fine_level2_amount: price of citation plus any late penalties or collections fees. Unpaid tickets can double in price and accrue a 22-percent collection charge.
* current_amount_due: total amount due for that citation and any related late penalties as of May 14, 2018, when data was last updated.
* total_payments: total amount paid for ticket and associated penalties as of May 14, 2018, when data was last updated.
* ticket_queue: This category describes the most recent status of the ticket. These are marked “Paid” if the ticket was paid; “Dismissed” if the ticket was dismissed, (either internally or as a result of an appeal); “Hearing Req” if the ticket was contested and awaiting a hearing at the time the data was pulled; “Notice” if the ticket was not yet paid and the city sent a notice to the address on file for that vehicle; “Court” if the ticket is involved in some sort of court case, not including bankruptcy; “Bankruptcy” if the ticket was unpaid and included as a debt in a consumer bankruptcy case; and “Define” if the city cannot identify the vehicle owner and collect on a debt. Current as of May 14, 2018, when the data was last updated.
* ticket_queue_date: when the “ticket_queue” was last updated.
* notice_level: This field describes the type of notice the city has sent a motorist. The types of notices include: “VIOL,” which means a notice of violation was sent; “SEIZ” indicates the vehicle is on the city’s boot list; “DETR” indicates a hearing officer found the vehicle owner was found liable for the citation; “FINL” indicates the unpaid ticket was sent to collections; and “DLS” means the city intends to seek a license suspension. If the field is blank, no notice was sent.
hearing_disposition: outcome of a hearing, either “Liable” or “Not Liable.” If the ticket was not contested this field is blank.
* notice_number: a unique ID attached to the notice, if one was sent.
* officer: a unique ID for the specific police officer or parking enforcement aide who issued the ticket.
address: full address of the form “<XXXX Streetname>, Chicago, IL <ZIP code>”. Addresses in this field are normalized to the block level (e.g. 1983 N. Ashland is transformed to 1900 N. Ashland) for more efficient geocoding and analysis. This field was computed by ProPublica and does not exist in the original data.

