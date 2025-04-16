# LLM-Metadata-Extraction-Paper-2025

Materials for the paper "Large Language Models Can Extract Metadata for Annotation of Human Neuroimaging Publications" (submitted to Frontiers in Neuroinformatics).

## Setup

The notebooks provided expect to have a `.env` file in the GitHub root folder that contains the following lines:

```text
ROOT_DIR=[Full path to folder containing GitHub clone]
LIB='Library'
OPENAI_API_KEY='Your OpenAI key'
```

Failure to set this environment will require modifying notebook files to make them work. Please note that we have attempted to make the notebooks also accept environment settings from other locations, so they _may_ work if you simply set these an environment variables directly.

## Organization

### Library Folder

The library folder contains the pre-processed input text used in the study. This is the text of each paper from the title through the end of the methods sections of the papers sent to the LLM via the OpenAI API. (Note that for copyright and other reasons the raw PDFs are not provided, but are all available from PubMedCentral.)
