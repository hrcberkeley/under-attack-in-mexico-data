
# Security apparatus

An organizational chart of Mexico's security and intelligence agencies:
446 units, based on 13 sources (news reports, official
publications and leaked Ministry of Defense documents).

| File | Rows |
|---|---:|
| `conflicting_source_pairs.csv` | 3 |
| `security-apparatus.json` | JSON |
| `sources.csv` | 13 |
| `units.csv` | 446 |

## units.csv

One row per unit.

| Column | Meaning |
|---|---|
| `unit` | Unit number on the chart |
| `id` | Unique ID, used by `parent_id` |
| `name_en`, `name_es` | Name in English and Spanish |
| `parent_id` | ID of the unit it reports to (empty for the top) |
| `second_superiors` | Other units some sources say it reports to |
| `sources`, `source_names` | Sources that describe the unit (IDs from `sources.csv`) |
| `conflicts_with_sources` | Sources that describe the unit differently |
| `cerfi_member` | True if the unit is part of or reports to the intelligence fusion centers (CERFI) |
| `feeds` | ID of the unit it sends intelligence to |
| `note` | Note from the chart |

## Other files

- `sources.csv`: the sources, with dates and links where public. `kind` is
  `open` (public), `internal` (not public) or `sdna` (leaked Ministry of Defense documents).
- `conflicting_source_pairs.csv`: pairs of sources that describe the same units
  differently.
- `security-apparatus.json`: the full chart.

## Notes

- Unit names are kept as the sources give them.
- When sources disagree, both versions are kept.
