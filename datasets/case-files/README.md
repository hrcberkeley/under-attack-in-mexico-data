
# Case files

75 cases of killings and other attacks on journalists and human
rights defenders. The text comes from the account «Targeted Killings and
Physical Violence».

| File | Rows |
|---|---:|
| `case-files.json` | JSON |
| `footnotes.csv` | 803 |
| `incidents.csv` | 75 |
| `narrative_paragraphs.csv` | 248 |
| `outcome_taxonomy.csv` | 10 |
| `persons.csv` | 95 |
| `timeline.csv` | 707 |

## incidents.csv

One row per case.

| Column | Meaning |
|---|---|
| `record` | Case number (CF-001 to CF-075) |
| `title`, `heading` | Name of the case and its full heading |
| `date_start`, `date_end`, `date_precision`, `date_as_written` | When it happened |
| `states`, `place` | Where it happened |
| `outcome` | Main outcome (for example, Killed) |
| `categories` | All outcomes recorded for the case |
| `identity` | Who the person was |
| `status` | Latest status of the investigation |
| `beats` | What the person reported on |
| `pattern_*` | True if the account places the case in that pattern |
| `paragraphs`, `words`, `footnotes` | Length of the case text |

## Other files

- `persons.csv`: every person named in a case (95 rows).
  `victims_record` links to `../victims/victims.csv` (34 people).
  Names are matched exactly, with dates no more than three days apart.
- `timeline.csv`: dated events in each case, with the quote and paragraph each
  one comes from.
- `narrative_paragraphs.csv`: the full text of each case. `para` is the
  paragraph number in the source document.
- `footnotes.csv`: the footnotes cited in the case text.
- `outcome_taxonomy.csv`: the list of outcomes and how each is defined.
- `case-files.json`: all fields for every case.

## Notes

- The case text for two cases gives the age of a minor.
