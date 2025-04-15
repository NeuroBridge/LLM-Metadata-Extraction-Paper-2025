# Task 1: General Imaging Type

This task was run manually at the ChatGPT interface to the GPT-4o model and therefore the materials provided here are different from the other experiments:

+ We used the PubMedCentral (PMC) provided PDFs of the publications analyzed, which were uploaded (as PDF files) to the GPT-4o model via the ChatGPT user interface. (Due to rules of use we do not provide the PDFs of the publications here, but they are easily available from PMC. Their PMCID numbers are provided in the spreadsheets in this folder.)
+ The prompt was cut-and-pasted to the ChatGPT interface. The prompt is in the file `task_prompt.txt`.
+ If the LLM failed to provide correct responses, it was then given the prompt "Please summarize this paper" and then, after the summary was generated, the original prompt was repeated verbatim and the LLM's revised answer scored. This affected 9 papers in total.

We note that:

+ If this approach was to be used programmatically, the two-pass procedure of (1) asking for a summary and then (2) passing the desired prompt could be implemented at the API.
+ Informal testing showed that this gave the same responses as the actual procedure used.

Provided here are three XLSX files that summarize the results of the experiment:

+ `mriTypeExamplesGpt4oManualRun.xlsx` contains the results of the GPT-4o analyses (only).
+ `mriTypeExamplesStudentRaw.xlsx` contains the student annotators' labeling (only).
+ `mriTypeExamplesDetailedErrors.xlsx` contains all of the above in one sheet with all of the specific errors highlighted for human inspection. If you want to see the full results of the experiment in one place this is the file you want.
+ This file has conditional formatting to highlight errors for the two types of LLM annotations and the student annotations based on the fixed ground truth/gold standard labels:
  + Any cells highlighted in red are cells for that condition that disagree with the ground truth.
  + Additionally, for the two types of LLM results (with and without summary) bold-italic type is used to highlight differences between these two conditions.

Note that the first column of each spreadsheet contains the list of PMCID numbers for the publications.

## Spreadsheet Column Codes

The codes for the sources of the annotations are:

+ GT - Ground Truth (Gold Standard) Labels
+ Student - Annotations by the student annotators
+ Hard - LLM annotations **before** summarization (LLM without summary)
+ Soft - LLM annotations **after** summarization (LLM with summary)

The codes for imaging types are as follows:

+ T1 - T1 Weighted Images
+ rsMRI - Resting State MRI
+ TPI - "Task Paradigm Imaging" (Referred to as task based MRI in the paper.)

Each column in the spreadsheet (12 total) is a combination of the code for the source of the annotations with the code for the imaging type (e.g. `GT_T1`, `Soft_TPI`, `Student_rsMRI`, etc.).
