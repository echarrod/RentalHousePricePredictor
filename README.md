# UK House Rental Price Predictor

## About
Predicting the rental price the following property features of UK houses:
- longitutude
- latitude
- bedrooms
- size (metres squared)
- dwelling type
- has garden

Using this date, this notebook looks at comparing basic price estimators, and calculating the importance of each of the above features with regards to price.

## Requirements

- Written in Python `2.7`, some alterations might be required for `3+`
- `numpy` `pandas` `scikit-learn` `matplotlib` `collections` `pygeocoder`
- Jupyter Notebook

## Installation

The easiest way to retrieve the requirements for this project is with the [anaconda](https://anaconda.org/)/[miniconda](https://conda.io/miniconda.html) python distribution, as it simplifies the setup process for scientific computation libraries such as `numpy` and `scikit-learn`.

### anaconda/miniconda users

If you use python distribution based on anaconda or miniconda based environment, first, install required packages by `conda` command:

```bash
$ conda install numpy pillow scipy pandas scikit-learn matplotlib pip
```

Jupyter Notebook can be installed with the Conda installer if you have Anaconda or Miniconda installed:

    $ conda install jupyter notebook

### pip
Alternatively you can use pip:

    $ pip install jupyter notebook


To open the notebook, `cd` to the directory that contains your code examples, e.g,.

    $ cd ~/directory/GTA

and launch `jupyter notebook` by executing

    $ jupyter notebook

Jupyter will start in our default browser (typically running at [http://localhost:8888/](http://localhost:8888/)), and you can explore the notebook from here.

## Future Work
- Obviously currently it's creating longitude and latitude as independent variables, when to get a more accurate regressor we should consider them together. I've started to look at extracting the first part of the post code from these with PyGeoCoder, which would give us a suitable feature to replace long & lat.
- We could train a model which would predict the time_on_market field, based on the rental price, in a similar way we've done here. So that you can adjust the rent to see how it would effect the esimated time on the market.
- Instead of looking at rental price, we could look at the difference with the national average for that time, e.g. £400/month in 2008 when the data first starts is a lot different to £400/month for the most recent listing this year. This could further be extended to compare it with the average price in the area using the coordinates.
Data from 2011 for the UK in general (including and excluding London as two separate figures) - https://www.ons.gov.uk/economy/inflationandpriceindices/bulletins/indexofprivatehousingrentalprices/july2017
Regional-specific data can be found here, but it wouldn't be as easy to integrate, as it doesn't look like they offer it in a Pandas-friendly format, we would need a web crawler - https://homelet.co.uk/homelet-rental-index
