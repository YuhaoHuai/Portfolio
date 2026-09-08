# Repository Guide

## Organization

Use this repository as a portfolio index and home for project summaries. Keep substantial code and hardware projects in their own repositories, linked from the corresponding project page. Argus and Bionic-Hand-Test-Device already have separate repositories.

For a small project stored directly here, use the following structure inside its existing project folder:

```text
projects/project-name/
  README.md
  src/             # Original application code or firmware
  cad/             # Original CAD and manufacturing exports
  electronics/     # Schematics and board files
  docs/            # Design notes and experiment reports
  media/           # Selected images and short demonstrations
  data/            # Small, documented example datasets
```

Create only the directories the project needs. Keep third-party reference projects separate and link to their originals.

## Add a project

1. Choose a descriptive English name and a lowercase folder name with hyphens.
2. Copy the project README template into the new folder.
3. Describe the problem, personal contribution, implementation, and evidence.
4. Add selected project assets or link to a dedicated source repository.
5. Add an entry to the project index and, when appropriate, the featured-project table.
6. Check that every local link points to an included file.

## Repository homepage

The portfolio is published in [11HYH11/Projects-Display](https://github.com/11HYH11/Projects-Display). Its root README is the project-display homepage, with detailed pages under `projects/`.

Link this repository from your GitHub profile and use its URL in application materials. If you later want a custom profile README, GitHub supports a separate public repository named `11HYH11`; that is optional and is not required to use this portfolio.

See [GitHub's official profile README guide](https://docs.github.com/en/account-and-profile/how-tos/profile-customization/managing-your-profile-readme).

## Material selection

Include project code, original design files, documented sample data, and selected images. Administrative documents and application materials do not belong in the portfolio. The local review notes are excluded by .gitignore.

Link to large recordings and datasets instead of copying entire working directories. Choose licenses separately for original code, hardware, and documentation; no blanket open-source license has been assigned in this draft.

