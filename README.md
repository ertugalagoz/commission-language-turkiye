# The Language of Conditionality

**How the European Commission has assessed Türkiye, 1998-2025**

A computational text analysis of the full run of the European Commission's annual
enlargement reports on Türkiye, measuring the Commission's own graded assessment
vocabulary rather than a sentiment dictionary.

**[Read the analysis](https://ertugalagoz.github.io/commission-language-turkiye/)**

## Summary

The Commission grades change in each policy area as no, limited, some, further or good
progress. Counting those qualifiers across twenty-seven annual reports gives a measure of
assessment that does not depend on a dictionary of the researcher's own making.

Three findings. The assessments were at their most lenient in 2004 and 2005, the years the
European Council decided that negotiations would open and they did, and the leniency is
sharpest in the political sections where conditionality bites hardest. The Commission has
judged political criteria more harshly than the technical chapters of the acquis in every
year of the period, by ten to twenty percentage points. And its political assessments
hardened substantially only after 2018, by which time the decline they describe had already
run its course.

A fourth claim is reported as having failed. The all-domain series reaches its most lenient
value in 2015, during the migration negotiations, but that softening disappears once the
measure is restricted to political criteria, and the migration interpretation is withdrawn.

## Reproducing the analysis

Requires R (4.1 or later) and Quarto.

```r
install.packages(c("tidyverse", "pdftools", "rvest", "remotes"))
remotes::install_github("vdeminstitute/vdemdata")
```

```
quarto render index.qmd
```

The extracted text of the reports is in `txt/` and the analysis runs from it. The chunk that
collects and extracts the PDFs is included in the document but is not executed on render,
since the source archives are reorganised periodically and a document that silently
re-downloads its corpus is one whose results can change unnoticed.

## Files

| File | Contents |
| --- | --- |
| `index.qmd` | Source document: prose and analysis code |
| `index.html` | Rendered output, served by GitHub Pages |
| `txt/` | Extracted text of the 27 reports, 1998-2025 |
| `references.bib` | Bibliography |

## Sources

Reports collected from the archive of the Turkish Directorate for EU Affairs and from the
European Commission's enlargement site. The reports are public documents of the European
Commission. Democracy indices from Coppedge et al., *V-Dem Country-Year Dataset v16*,
Varieties of Democracy Project, <https://doi.org/10.23696/vdemds26>.

## Companion piece

[Conditionality and Its Limits](https://ertugalagoz.github.io/turkey-eu-conditionality/),
on Türkiye's democratic trajectory across the accession process.

## Author

Ertuğ Alagöz

## Licence

Text and figures under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/); code under
the MIT Licence.
