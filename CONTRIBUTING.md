# Contributing

This guide is for Lender Center staff adding or updating a dataset file. It takes four parts: convert, write the caveats, check, and open a pull request.

## Before you start

1. Create a GitHub account if you don't have one.
2. Request membership in the SyracuseUniversity GitHub organization through MyAccess.
3. Ask ITS (aihelp@syr.edu) to add you to this repo.

## 1. Convert a spreadsheet with Claude

Work on one topic at a time. Each geography gets its own file.

1. Open the master sheet from the Lender Center SharePoint.
2. In Claude, attach the sheet, [`.github/dataset_template.md`](.github/dataset_template.md), and one finished file from `datasets/` as an example.
3. Ask for one Markdown file per geography in exactly the template's format. For example:

   > Convert the City of Syracuse columns of this sheet into one Markdown file that follows the attached template and matches the attached example. One row per indicator, at most four years per row, newest year first. Put the geography and the year span in every row label. Use `—` for missing values. List anything that looks wrong in the source (totals that don't add up, values that look summed or mislabeled) so I can review it.

4. Save the file as UTF-8 with the name `<topic>_<geography>.md`, for example `housing_city_of_syracuse.md`.

## 2. Write the caveats

Marvin follows the notes in each file over its own assumptions, so this part matters most. A Lender analyst decides what goes here, not Claude.

- **Who is counted:** persons, households or housing units; all ages or adults only.
- **Which denominator** to use for rates.
- **Source errors** and any figure you withheld, with what Marvin should say instead.
- **Groups that don't add up**, such as overlapping race and Hispanic-origin categories.
- **What the file leaves out.** Say it is absent, not zero.

## 3. File standard

Every file follows [`.github/dataset_template.md`](.github/dataset_template.md):

1. Title: `# Lender Center — <Topic>: <Geography>`
2. Metadata lines: Source, Data last updated, Geography, Years covered
3. A "Read this before using these figures" paragraph
4. A caveats section
5. Topic sections named `## <Geography> — <Section>`, each repeating the source line
6. Tables with one row per indicator. The row label names the geography, the indicator and the year span. Values are `year: value`, newest first, at most four years per row.

Rows repeat the geography and years because Marvin reads pieces of files, not whole files. A row has to make sense on its own.

**Size:** keep each file under about 8,000 tokens (roughly 30 KB). Split by topic or geography instead of making one large file.

**Names:** lowercase, underscores, no dates or version numbers. Git keeps the history.

## 4. Check and open a pull request

1. Compare at least five numbers in the file against the sheet, including the newest year.
2. Create a branch, add your file under the right `datasets/<topic>/` folder, and open a pull request.
3. Fill in the checklist in the pull request description.
4. A Lender Center data owner reviews and merges it.
5. After the next sync, ask Marvin a question the change should answer and check that it cites the new figure.

## Questions

Data content: lendercenter@syr.edu. Repo access or Marvin: aihelp@syr.edu.
