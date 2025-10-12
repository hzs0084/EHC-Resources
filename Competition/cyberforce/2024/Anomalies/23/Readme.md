# Anomaly 23 - Hold my Floaties
Challenge Description
The dependency file contains anomalous entries, these entries seem to be generating power when the windmill should not be able too. Find these entries and add the total electricity_produced between the anomalous entries to get the flag. It will be a float value.
NIST Category: Investigation - Conducts national cybersecurity and cybercrime investigations, including the collection, management, and analysis of digital evidence.

Solution
We are asked to find anomalies in data entries of a .csv where power is generated when it should not be. We are provided with an extensive .csv with 5000 rows of entries.
bash$ wc -l ICS_DataHistory_Anomaly.csv
5000 ICS_DataHistory_Anomaly.csv
From opening the CSV we see that the variable we are looking for anomalous data for is column 7.
timestamp         | sensor1_windspeed | sensor1_rotorspeed | sensor2_windspeed | sensor2_rotorspeed | activepower | electricity_produced | temperature | alarm_code
------------------|-------------------|--------------------|--------------------|--------------------|--------------|-----------------------|-------------|------------
1722524400        | -                 | 32.98              | 25.52              | 33.2               | 1572.88      | 262.15                | 42.54       | E4F3992C
1722525200        | 26.26             | 24.64              | 26.29              | 25.09              | 1452.93      | 242.16                | 36.78       | NULL
1722526000        | 28.04             | 34.24              | 27.66              | 34.98              | 1672.06      | 278.68                | 31.07       | 6E8FT065
...
If we are looking for times when electricity is purported as falsely produced, the other columns that should be a prerequisite for power production become prime suspects for investigation: namely columns 1-6.
I use an awk command to search for the first 6 columns for entries of zero (these may be times where it wouldn't make sense for the electricity produced to be nonzero)
bashawk -F',' '$1 == 0 || $2 == 0 || $3 == 0 || $4 == 0 || $5 == 0 || $6 == 0' file.csv
This command flags returns several entries from columns 3 and 5, showing they may be what we are searching for.
Next I run a command that shows the associated column 7 value and the row number for more information
bashawk -F ',' '($3 == 0 || $5 == 0) {print "Row " NR ": " $7}' ICS_DataHistory_Anomaly.csv
Here we add up the values of our anomalous entries and find the flag.
bash$ awk -F ',' '($3 == 0 || $5 == 0) {print "Row " NR ": " $7}' ICS_DataHistory_Anomaly.csv
Row 1093: 234
Row 1317: 258.54
Row 3012: 235.73
Row 4397: 254.29

$ python3
Python 3.12.3 (main, Aug 14 2025, 17:47:21) [GCC 13.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> print(234+258.54+235.73+254.29)
982.56
Flag
982.56
