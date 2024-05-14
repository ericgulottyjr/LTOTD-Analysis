# LTOTD-Analysis
This notebook is designed to perform analysis of last trip of the day (LTOTD) tagging by the MBTA OCS. 

## Required Files
The notebook requires 4 files to function, 3 of which require Splunk downloads, specific Splunk queries are commented within the notebook:
1. Splunk download of s-tagged trips
2. Splunk download of `TSCH NEW` messages for the Red, Blue, and Orange lines
3. Splunk download of all `TMOV` messages for the Red, Blue, and Orange lines from 11pm~2am (same revenue day)
4. `locations.csv` from latest [MBTA GTFS file](https://www.mbta.com/developers/gtfs), make sure to place the file in the same directory as the notebook.
5. Files 1~3 can be placed within a folder titled `Splunk_downloads/` in the same directory as the notebook, otherwise remove the folder from the path in the first cell and add the files to the same directory as the notebook instead.

## Output
The notebook will optionally output a `.csv` file with a name of the user's choosing, a `.csv` file extension is required at the end of the user-designated file name.

Another optional output is a graph which displays the number of unique `trip_id`s that were tagged on a given revenue day.
