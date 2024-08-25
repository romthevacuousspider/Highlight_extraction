# Key information extraction

This repository contains the implementation of a research project focused on extracting key information and facts from academic texts using Large Language Models (LLMs). The project was developed as part of the MA Computational Linguistics program at Goldsmiths, University of London in collaboration with Scholracy.

## Table of Contents
- [Project Overview](#project-overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Dataset](#dataset)
- [Models](#models)
- [Evaluation](#evaluation)
- [Contributions](#contributions)
- [Future Work](#future-work)
- [License](#license)
- [Acknowledgements](#acknowledgements)


# Project Overview
This project investigates the effectiveness of LLMs in extracting key information from academic texts, addressing the limitations of traditional rule-based methods. The research is focused on three levels of granularity: sentence level, segment level, and word level.

The key objectives of this project are:
- To evaluate the performance of LLMs in comparison to traditional rule-based methods.
- To explore the benefits and limitations of fine-tuning versus prompt-based approaches in LLMs.
- To identify challenges of extraction tasks and propose potential solutions on each level of granularity.

# Features
- **Sentence-Level Extraction:** Fine-tuned LLMs to classify sentences as either worth highlighting or not.
- **Segment-Level Extraction:** Utilized Seq2Seq models to extract important segments within paragraphs and prompting LLMs.
- **Word-Level Extraction:** Implemented CRFs, LSTM, and fine-tuned LLMs for word-level by treating key facts as a named entity.

# Installation
To install and run this project, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/romthevacuousspider/Highlight_extraction.git
   cd Highlight_extraction

2. Install the required dependencies:
   pip install -r requirements.txt

3. Set up your environment, particularly if you plan to fine-tune models or use GPUs:

    Ensure you have access to a GPU-enabled environment if necessary.
    Modify paths to datasets as required.

# Usage
## Running the Notebooks

The project includes several Jupyter notebooks that demonstrate the process of fine-tuning models, extracting highlights, and evaluating results.

    Sentence-Level Extraction:
        Navigate to the sentence_level directory.
        Open the fine_tuning_llama.ipynb notebook and follow the instructions.

    Segment-Level Extraction:
        Navigate to the segment_level directory.
        Use the t5_finetuning.ipynb notebook to run the segment-level extraction model.

    Word-Level Extraction:
        Navigate to the word_level directory.
        Execute the crf_lstm_extraction.ipynb notebook.

Running the Models via API

For using the models programmatically, refer to the examples provided in the OPEN AI API folder for guidance on how to call the models via an API.
