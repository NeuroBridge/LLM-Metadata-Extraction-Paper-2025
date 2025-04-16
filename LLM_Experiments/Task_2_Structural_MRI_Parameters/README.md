# Task 2: Structural MRI Parameters

## Summaries and Data

The following files contain the experimental results:

+ `ground_truth_structural_mri_parameters_final.csv` contains the final ground truth/gold standard data. See paper for details.
+ `LLM_annotations_structural_MRI_parameters.csv` contains the results of the LLM labeling.
  + The raw JSON of these results is in the `Results` folder.
+ `human_annotations_structural_mri_parameters.xlsx` contains the human annotators work and indicates the locations of the student errors during development. (Note that the locations no longer contain the original errors as this sheet was corrected during development.)

## Prompt & JSON

+ The prompt is in the file: `prompt.txt`.
+ The JSON is in the file: `prototype.json`.

# Code

+ The notebook `run_T1_MRI_Parameters_GPT-4o.ipynb` accesses the LLM via the API and runs the experiment.
+ The notebook `convert_MRI_JSON_parameters_to_CSV.ipynb` converts the JSON returned from the API and makes it into a CSV file for comparison with the gold standard data.