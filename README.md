# dc-campaign-finance-dedupe

Attempt to use [csvdedupe](https://github.com/datamade/csvdedupe) from the [dedupe](https://github.com/datamade/dedupe) project to normalize the `Contributor Name` in DC Campaign Finance Data.

The parent project is [DC Campaign Finace Watch](https://github.com/codefordc/dc-campaign-finance-watch) part of [CodeForDC](http://codefordc.org/).

![](http://puu.sh/mt6gd/1b81d735b3.png)

## Setup

This project uses Python 3.5.X with numpy. Having Node installed would also be helpful.

```
pip3 install --upgrade numpy
pip3 install --upgrade csvkit
pip3 install --upgrade csvdedupe
```

## Usage

**View Deduped Data**

- Open `output.csv` in Excel.
- Sort by `Cluster ID` (the first column).

**Dedupe**
```
csvdedupe DC_contribs_since_2007.csv --field_names "Contributor Name" --output_file output.csv
```

**Check number of training examples completed**
```
node -p "x = require('./training.json'); x['distinct'].length"
```

**Extract high level descriptive stats from CSV**
```
csvstat DC_contribs_since_2007.csv
``` 

--------------------------------------------------

## Beginner Setup
```
brew install python
brew install homebrew/python/numpy
brew install node
```