#ETL Presentation (rough outline)

## Extract
Primary data sources: Los Angeles Crime & Arrest Data (Kaggle) and UFO Sightings, from the National UFO Reporting Center or NUFORC (Kaggle)
Format: CSV files (738 MB and 28 MB)
- Datasets picked for a broad set of data with date/time stamps and location information--possible data query use/joins
- Location of the "crime" dataset determined based on the state with the most UFO sightings (California)

## Transform
Types of transformation needed: cleaning and filtering
- Reduced the number of columns to remove:
1. excess/redundant data
2. specific coding (lack of documentation for our own use)
3. weird data types
- Dropped rows with missing data or NaNs
- Filtered results down to California
- Converted the date-time columns to date-only datetime objects
- Restricted datasets from date of earliest crime data available to lastest UFO sighting data available

## Load
The final database used: PostgreSQL
- Two tables created, UFO and Crime, with table schema queries
- PGAdmin was used for ease of coding/familiarity through Jupyter Notebook
- Also picked for practical application (can easily demonstrate joins between tables on particular dates/periods of time)
