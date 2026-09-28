
# Victims

337 journalists and human rights defenders killed in Mexico between
December 2018 and September 2024: 259 human rights and environmental defenders, 78 journalists.

| File | Rows |
|---|---:|
| `bibliography_mentions.csv` | 192 |
| `source_links.csv` | 719 |
| `victims.csv` | 337 |
| `victims.json` | JSON |

## victims.csv

One row per person.

| Column | Meaning |
|---|---|
| `record` | Record number (V001 to V337) |
| `workbook_id` | ID in the source workbook (H = defender, J = journalist, A = added from researchers' lists) |
| `name` | Name |
| `category` | `journalist` or `hr_environmental_defender` |
| `disposition` | What happened (Killed) |
| `date`, `date_precision` | Date of death |
| `state`, `city` | Where |
| `outlet`, `beat` | Where a journalist worked and what they covered |
| `case_files` | Case number in `../case-files/`, if there is one |
| `summary` | Short case summary written by the researchers |

## Other files

- `source_links.csv`: links to reporting on each death (719 links).
- `bibliography_mentions.csv`: works in the project's bibliography that name the
  person (192 rows).
- `victims.json`: the same records.

## Notes

- Values are kept as the researchers recorded them.
- Some summaries give the age of a minor.
- This folder has no data from the mañaneras.
