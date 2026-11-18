# Munich air quality and temperature

Status: work in progress.

## Question
How are NO2 and PM10 concentrations at Munich monitoring stations related to air temperature in 2025?

## Data
- Air quality: Umweltbundesamt (UBA) Luftdaten API, hourly values, 2025.
  Source: "Umweltbundesamt mit Daten der Messnetze der Länder und des Bundes".
  Licence: Datenlizenz Deutschland - Namensnennung - Version 2.0 (as listed in the catalouge record for the API; to be re-checked at the end).
- Temperature: Deutscher Wetterdienst (DWD) Climate Data Center, station München-Stadt (03379), hourly.
  © Deutscher Wetterdienst. Licence: TODO (check DWD's terms).

## How to reproduce
TODO (fill in at the end).

## Data quality notes
- DWD marks missing values with -999. These were converted to empty values: 99 hours of temperature over 1997 to 2025, 72 of them in 2025.
- Temperature gaps in 2025: one continuous gap of 69 hours (22 April 2025 13:00 UTC to 25 April 2025 09:00 UTC) and 3 single missing hours in November. The gaps were left empty and not filled.
- Time zones: DWD times are in UTC. The UBA documentation says CET/CEST, but the clock-change days in 2025 (30 March, 26 October) both have 24 hourly values, which suggests a fixed UTC+1. This is an assumption. TODO (what we did about it: converted to UTC before joining).
- Air quality gaps: not all hours are present. For example, Lothstraße NO2 has 8591 of 8760 values.
- Allach (DEBY189): no PM10 data found in 2025.
- PM10 above 100 µg/m³ occurred in 28 hours: 21 on 1 January (most likely New Year's fireworks), 5 on 9 December at three stations (cause unknown), 1 on 24 January, 1 on 7 August. These values were kept.
- Join: NO2 and temperature were joined on the hour (UTC). 288 NO2 rows have no temperature (72 hours × 4 stations).

## Results
TODO (after the analysis).

## Limitations
TODO

## AI assistance
TODO 