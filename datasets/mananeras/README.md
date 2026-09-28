
# Mañaneras

The President's morning press conferences («mañaneras») from December 2018 to
September 2024, and the hostile statements he made about the press in them.

- 1,437 press conferences on 1,436 dates (two were held on
  one day).
- 2,827 hostile statements, found with a list of 49
  Spanish terms (version 1.2.0).
- 67 notable incidents, selected and summarized by researchers.

| File | Rows |
|---|---:|
| `categories.csv` | 4 |
| `dimensions.csv` | 6 |
| `documents.csv` | 1,170 |
| `emblematic_incidents.csv` | 67 |
| `instances.csv` | 2,827 |
| `mananeras.csv` | 1,436 |
| `mananeras.json` | JSON |
| `terms.csv` | 49 |

## How a statement was counted

A passage counts when both are true:

1. It contains at least one term from the list.
2. The President said it. Statements by reporters, officials and others are
   not counted.

Some terms count only when the same passage also mentions the press or names a
journalist or outlet.

## mananeras.csv

One row per date.

| Column | Meaning |
|---|---|
| `date` | Date |
| `held` | Number of press conferences that day |
| `transcript_listed` | Whether this date's transcript is in `documents.csv` |
| `instances` | Number of hostile statements. Empty when `transcript_listed` is false (386 dates). |
| `terms` | Terms used that day |
| `emblematic_incidents` | IDs of notable incidents that day |
| `transcript_url`, `wayback_url` | Links to the official transcript and an archived copy |

## instances.csv

One row per statement.

| Column | Meaning |
|---|---|
| `date`, `document`, `document_kind` | Where it was said. `document_kind` is `matutina` (press conference) or `discurso` (speech). |
| `segment`, `segment_key` | Part of the event (see below) |
| `score` | Sum of the term weights (1 to 3 each) |
| `terms`, `dimensions`, `categories` | Which terms matched and how they are grouped |
| `named` | Journalists or outlets named in the passage |
| `excerpt_es` | The passage in Spanish, as transcribed |
| `transcript_url`, `wayback_url` | Links |

Segments:

| Key | Meaning | Statements |
|---|---|---:|
| `exchange_a` | exchange with the press | 2,544 |
| `about_press` | about the press | 268 |
| `mentiras_segment` | ¿Quién es quién en las mentiras? | 15 |

## Other files

- `terms.csv`: the term list, with English glosses, weights and yearly counts.
  46 of the 49 terms were used.
- `dimensions.csv`, `categories.csv`: how terms are grouped. A statement with
  terms from several groups counts in each group.
- `emblematic_incidents.csv`: notable incidents with English summaries and links.
- `documents.csv`: the 1,170 transcripts that contain at least one hostile statement.
- `mananeras.json`: all of the above.

## Notes

- `documents.csv` lists only transcripts that contain at least one hostile
  statement. The original corpus has a transcript for every press conference,
  so an empty `instances` cell most likely means none were found that day. The
  dataset alone cannot confirm this, so those cells are left empty, not set to 0.
- 120 of the transcripts are speeches, not press
  conferences. Filter on `document_kind` to exclude them.
- The dimension «Gendered attack» has no terms, so its count is always zero. This does
  not mean no such statements were made.
- The `firstUse` date for some terms in `mananeras.json` counts use by anyone,
  not only the President. Use `instances.csv` for the President's first use.
- This folder has no data from the victims or case-file folders.

## License

CC BY-NC-SA 4.0. See `LICENSE`. Transcripts: official stenographic versions,
collected by NOSTRODATA (nostrodata.com, CC BY-NC-SA 4.0, credit @nostrodata)
and the Internet Archive's Wayback Machine.
