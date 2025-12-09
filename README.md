# USGS Streamflow Tools

This repository contains a collection of Python tools for downloading, processing,
interpolating, and visualizing **USGS NWIS Instantaneous Values (IV) streamflow data**.
The primary purpose is to support **sink–rise hydrologic analysis**, where discharge
from two hydrologic stations is compared through time.

The repository includes an interactive **Google Colab notebook**, which allows users to:

- Retrieve USGS discharge data for any gauge station
- Specify start/end date ranges
- Interpolate time series to a uniform time grid
- Plot the sink, rise, and sink–rise difference curves
- Explore flow dynamics without installing anything locally


---

## Launch Interactive Notebook in Google Colab

Click below to run the tool directly in your browser:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](
https://colab.research.google.com/github/yoon-group/usgs_tools/blob/main/sink_rise_discharge.ipynb
)

No installation is required — everything runs in the cloud via Google Colab.


---

## 📘 Features of the Notebook

### Retrieve USGS IV Data  
- Uses the official USGS NWIS Instantaneous Values API  
- Retrieves discharge (`00060`) by default  
- Works with any station with IV data available  

### Interpolation of Time Series  
Sink and Rise data may have slightly inconsistent timestamps.  
The notebook:

- Creates a common time grid (`15min` default)
- Interpolates both series using time-based interpolation
- Computes Sink and Rise discharge differences
- Produces smooth plots

### Interactive UI via `ipywidgets`  
Users can edit:
- Start date  
- End date  

The UI updates the plots dynamically.

---
