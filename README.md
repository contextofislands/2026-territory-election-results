# 2026 territory election results

Results of the Nov. 3, 2026 general election in **Guam**, the **Northern Mariana Islands** and the **US Virgin Islands**, as posted by each territory's election office, read and compiled by [Pasquines](https://pasquines.us), a nonprofit newsroom covering the US territories.

A watcher checks each election office every minute. When a new report appears, it is parsed and committed here within about a minute, so this repository keeps every version of the count, with the time we read it.

Live results maps: [Guam](https://pasquines.us/2026-elections/guam/) · [Northern Mariana Islands](https://pasquines.us/2026-elections/northern-mariana-islands/) · [US Virgin Islands](https://pasquines.us/2026-elections/us-virgin-islands/)

## Files

| Path | What it is |
|---|---|
| `data/<territory>/latest.json` | The newest report, parsed: every race, candidate totals, and results by precinct (or election district) where the office reports them |
| `data/<territory>/latest.csv` | The same as a flat table: `territory, precinct, contest, party, office, candidate, votes` |
| `data/<territory>/archive/<time>.json` | Each report as we read it; the file name is the UTC time it was read |
| `data/calls.json` | Pasquines' race calls: `Projection`, `Final`, `Runoff`, or an automatic `Presumptive` call (`"auto": true`) made when every precinct is in and the margin is more than 1 point |

`<territory>` is `guam`, `northern-mariana-islands` or `us-virgin-islands`.

## Sources

| Territory | Election office | Where results are posted |
|---|---|---|
| Guam | Guam Election Commission | [gec.guam.gov](https://gec.guam.gov/2026-general-election-info/) |
| Northern Mariana Islands | Commonwealth Election Commission | [votecnmi.gov.mp](https://www.votecnmi.gov.mp/election-results-archive/2026-election-results) |
| US Virgin Islands | Elections System of the Virgin Islands | [vivote.gov](https://vivote.gov/?elections=2026-general-election) |

Each JSON file names its source document in `source.url`, with the time we read it (`source.fetched_at`) and a SHA-256 hash of the original file.

## Notes

- Results are **unofficial** until each office certifies them. `report.status` says `UNOFFICIAL` or `OFFICIAL` as printed on the report.
- Names, race titles and precinct names are spelled as the election office printed them.
- The US Virgin Islands reports territory-wide totals by type of ballot (Election Day, early, absentee, provisional), not by precinct, unless it posts a precinct report.
- The Northern Mariana Islands reports early voting (`EV`) and absentee ballots (`ABS`) as their own columns, next to the 13 election districts.
- Calls in `calls.json` are Pasquines' editorial judgment, not official results.

## Use and credit

The data compilation is licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Please credit: **"Source: [election office]; compiled by Pasquines (pasquines.us)."**

Corrections and questions: context@pasquines.us
