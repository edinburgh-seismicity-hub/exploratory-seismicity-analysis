# exploratory-seismicity-analysis
Examples of how to explore the properties of seismic catalogues

In these examples, we are interested in how we can analyse real seismic catalogues. This is often a starting point for studies of seismicity as it is important to understand their basic features and identify potential sources of uncertainty and bias.


The purpose of such analyses is often to extract a smaller subset of a large catalogue for deeper analysis. Hence, the workflow is typically:

- Load a catalogue
- Sort out how to parse the date-times
- Make various exploratory plots
- Pick an interesting subset of the data
- Export that catalogue subset for further analysis

The notebooks will take us through this process. Deeper analyses of specific sequences will be done in other projects hosted here.

## Case Studies

- R Markdown example of exploratory data analysis for a New Zealand catalogues

## Typical outputs

We produce a range of graphical and statistical outputs including:

- Spatial maps of events with coastline
- Spatial density plots with coastline
- Magnitude time series
- Frequency-Magnitude analysis including b-value stability
- Latitude-time plots
- Demonstration of analysis at both a national and regional level
