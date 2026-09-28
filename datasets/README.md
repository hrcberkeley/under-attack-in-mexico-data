
# Under Attack in Mexico: datasets

Data from *Under Attack in Mexico*, a case dossier on attacks against journalists and human
rights defenders in Mexico from December 2018 to September 2024. Made by
The Human Rights Center, UC Berkeley School of Law.

## What's here

| Folder | Contents | Rows |
|---|---|---:|
| [`case-files/`](case-files/) | Case files on killings and other attacks | 75 cases |
| [`victims/`](victims/) | Journalists and human rights defenders killed | 337 people |
| [`mananeras/`](mananeras/) | The President's morning press conferences and his hostile language about the press | 1,436 dates, 2,827 statements |
| [`security-apparatus/`](security-apparatus/) | Organizational chart of Mexico's security and intelligence agencies | 446 units |

Each folder has CSV files, one JSON file with the full records, and its own
README describing the files and columns.

`MANIFEST.json` lists every file with its size, row count and SHA-256 checksum.

## Conventions

- Dates use the format YYYY-MM-DD. Where a source gives only a month or year,
  the date is shortened (YYYY-MM or YYYY) and a `*_precision` column says so.
- An empty cell means the source does not give that value. It does not mean zero.
- Where a cell holds a list, the items are separated by `; `.
- Text quoted from sources is reproduced exactly, including spelling.
- Known errors in the sources are kept and noted in each folder's README. They
  have not been corrected.

## Linking the folders

- `case-files/persons.csv` has a `victims_record` column that matches `record`
  in `victims/victims.csv`.
- `victims/victims.csv` has a `case_files` column that matches `record` in
  `case-files/incidents.csv`.
- The mañaneras data is not linked to the victims or case-file data. The
  datasets do not connect any statement by the President to any attack.

## License

- `case-files/`, `victims/` and `security-apparatus/`: CC BY 4.0 (see `LICENSE`).
- `mananeras/`: CC BY-NC-SA 4.0 (see `mananeras/LICENSE`). This is required by
  the license of the transcripts it is built from.
- Quoted text belongs to its original authors and publishers.

Please cite as: The Human Rights Center, UC Berkeley School of Law, *Under Attack in Mexico* datasets (2026).
