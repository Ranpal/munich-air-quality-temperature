# Munich air quality and temperature

Status_work in progress.

## Question
How are NO2 and PM10 concentrations at Munich monitoring stations related to air temperature in 2025?

## Data
- Air quality: Umweltbundesamt (UBA) Luftdaten API, hourly values, 2025.
  Source: "Umweltbundesamt mit Daten der Messnetze der Länder und des Bundes".
  License: Datenlizenz Deutschland - Namensnennung - Version 2 (as listed in the catalouge recourd for the API; to be re-checked at the end).
- Temperature: Deutscher Wetterdienst (DWD) Climate Data Center, station München-stadt (03379), hourly.
  © Deutscher Wetterdienst. Licence: TODO (check DWD's terms).

## How to reproduce
TODO (fill in at the end).

## Data quality notes
- DWD marks missing values with -999. These were converted to empty values: 99 hours of temperature over 1997 to 2025, 72 of them in 2025.
- UBA times are in local time (CET/CEST), DWD times are in UTC. TODO (what we did about it).
- Allach (DEBY189): no PM10 data found in 2025.
- The April 2025 temperature gap: One continuous gap of 69 hours from 22 April 2025 13:00 ITC to 25 April 2025 09:00 UTC and 3 single missing hours in November, 2025. The gaps were left empty and not filled.

## Results
TODO (after the analysis).

## Limitations
TODO (at least three points).

## AI assistance
TODO
