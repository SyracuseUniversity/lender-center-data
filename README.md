# Lender Center Data

Public datasets from the [Lender Center for Social Justice](https://lendercenter.syr.edu) at Syracuse University, written as Markdown files.

**Marvin**, the Lender Center's data mentor on [mentorAI](https://mentor.ai.syr.edu), reads the `main` branch of this repo. Marvin answers community questions from these files and cites the source and date in each one. When a change is merged to `main`, Marvin picks it up at its next sync.

## What's here

```
datasets/
  housing/        housing_<geography>.md
  education/      education_<geography>.md
  disability/     disability_<geography>.md
  demographics/   demographics_<geography>.md
  veterans/       veterans_<geography>.md
  comparisons/    comparison_<topic>_by_geography.md
```

Geographies used in file names:

| Slug | Place |
| --- | --- |
| `united_states` | United States |
| `new_york_state` | New York State |
| `central_new_york` | Central New York (Cayuga, Cortland, Madison, Onondaga and Oswego counties) |
| `onondaga_county` | Onondaga County |
| `city_of_syracuse` | City of Syracuse |
| `cayuga_county` | Cayuga County |
| `cortland_county` | Cortland County |
| `madison_county` | Madison County |
| `oswego_county` | Oswego County |

## Rules

- **Public data only.** No restricted, licensed or personal data, ever. Anything in this repo can be read by anyone and is answered from by Marvin.
- **No raw spreadsheets.** The master Excel files stay in the Lender Center's SharePoint. Only reviewed Markdown goes here.
- **Every change goes through a pull request** and needs approval from a Lender Center data owner before it reaches `main`.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for how to convert a spreadsheet to Markdown, the file standard, and the review checklist.

## Who to contact

- Data content: the Lender Center for Social Justice, lendercenter@syr.edu
- Repo settings and the Marvin connection: ITS Enterprise Data & AI Team, aihelp@syr.edu
