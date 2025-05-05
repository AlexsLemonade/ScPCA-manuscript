# Contribution guidelines for the ScPCA Manuscript

This manuscript is written using the Manubot framework.
Please see [`USAGE.md`](USAGE.md) for information on how writing manuscripts with Manubot. to use the Manubot platform for writing the manuscript.

## Manuscript style

Please follow these stylistic guidelines when updating this manuscript.

### Tense

* Use past tense when referring to analyses performed or actions previously taken to build the Portal, process data, develop the pipeline, etc.
* Use present tense when referring to current ScPCA Portal contents or downloads.

### Voice

Note that these are general guidelines, but we do not have to be overly rigid about enforcing them.

We generally prefer active voice, but passive voice is acceptable when describing tasks very literally performed by code, e.g. a step or process in the `scpca-nf` workflow, a technical analysis, or any action that cannot clearly be ascribed to a single individual or team.
Otherwise, you should aim to write in the active voice unless it negatively impacts communication/clarity.

Here are some examples of acceptable uses of passive voice:

* This is a sentence that is literally describing a step that code is taking:
    * _The unfiltered gene by cell counts matrices are filtered to remove any barcodes that are not likely to contain cells using `DropletUtils::emptyDropsCellRanger()`._
* This is a sentence whose meaning is communicated clearly enough in passive voice that it's ok to have:
  * _The largest number of samples found on the Portal were obtained from patients with leukemia (n = 216)._

* This is a Methods sentence describing a technical analysis step:
  * _Organ-specific references were built using all cell types in a specified organ listed in `PanglaoDB`._

## Miscellaneous

* When using the phrase "et al.", write it in plain text as shown here (not in italics)
* When updating manuscript numbers based on Portal changes, refer to these tables for the most up-to-date numbers: https://github.com/AlexsLemonade/scpca-paper-figures/tree/main/manuscript-numbers
* Ensure the `scpca-paper-figures` repository tag is up-to-date in [`content/100.figure-table-legends.md`](./content/100.figure-table-legends.md)

