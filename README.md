# Comedian Trends

A Flask dashboard over Google Trends search-interest data, rendered with Plotly.

Pick a date range and the app re-slices the series and redraws the charts server-side,
handing the frontend a JSON figure rather than raw rows.

## Running it

```bash
pip install -r requirements.txt
python app.py
```

Then open http://localhost:5000.

## Notes

`trends_data.csv` holds monthly search interest exported from Google Trends
(December 2019 onward). The loader normalises `YYYY-MM` values to real dates and
degrades to an empty frame with a logged error if the file is missing, so the app
still starts.

## Stack

Python · Flask · pandas · Plotly
