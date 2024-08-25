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


# Project Overview
<a id="project-overview"></a>
This project investigates the effectiveness of LLMs in extracting key information from academic texts, addressing the limitations of traditional rule-based methods. The research is focused on three levels of granularity: sentence level, segment level, and word level.

The key objectives of this project are:
- To evaluate the performance of LLMs in comparison to traditional rule-based methods.
- To explore the benefits and limitations of fine-tuning versus prompt-based approaches in LLMs.
- To identify challenges of extraction tasks and propose potential solutions on each level of granularity.

# Features
<a id="features"></a>
- **Sentence-Level Extraction:** Fine-tuned LLMs to classify sentences as either worth highlighting or not.
- **Segment-Level Extraction:** Utilized Seq2Seq models to extract important segments within paragraphs and prompting LLMs.
- **Word-Level Extraction:** Implemented CRFs, LSTM, and fine-tuned LLMs for word-level by treating key facts as a named entity.

# Installation
<a id="installation"></a>
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
<a id="usage"></a>
## Running the Notebooks

The project includes several Jupyter notebooks that demonstrate the process of fine-tuning models, extracting highlights, and evaluating results.

- Sentence-Level Extraction:
      - Navigate to the `Sentence-level` directory.
      - Navigate to the `Llama3` folder, open the `Llama3_fine_tuning_att1.ipynb` and `Llama3_fine_tuning_att2.ipynb` notebooks, and follow the instructions for fine-tuning Llama3.
      - Navigate to the `Open AI API` folder, open the `OpenAI_Fewshot.ipynb` and follow the instructions for prompting GPT4.5o.
      - Navigate to the `Scholracy` folder, open the `Scholracy_F1_test.ipynb`, and follow the instructions for the baseline evaluation.

- Segment-Level Extraction:
      Navigate to the `Segment-level` directory.
      Navigate to the `T5` folder, open the `T5_fine_tuning.ipynb` notebook, and follow the instructions for fine-tuning T5.
      Navigate to the `Llama 3 (playground test)` folder, open the `Groq_Llama_3_Playground_Rouge_test.ipynb` and follow the instructions for evaluating.
      Navigate to the `Scholracy` folder, open the `Scholracy_Rouge_test.ipynb`, and follow the instructions for the baseline evaluation.

- Word-Level Extraction:
      Navigate to the `Word-level (IOB)` directory.
      Navigate to the `Llama3` folder, open the `IOB_&_Llama3.ipynb` notebook, and follow the instructions for fine-tuning Llama3.
      Navigate to the `LSTM` folder, open the `LSTM_IOB_classification.ipynb` and follow the instructions for defining LSTM models.
      Navigate to the `CRF` folder, open the `CRF.ipynb`, and follow the instructions for the CRF evaluation.

## API Key

An API key is needed to use the GPT4.5o programmatically and fine-tune the Llama3.

# Dataset
<a id="dataset"></a>

The datasets used in this project are annotated academic papers across various subjects, including social sciences, arts, literature/philosophy, medical/biology, and applied physics. The data was manually annotated for sentence, segment, and word levels.

# Models
<a id="models"></a>

The project utilizes the following models:

- GPT-4.5o: Used for sentence-level classification via prompt and few-shot learning.
- Llama 3-8B and Llama 3-70B: Fine-tuned Llama3-8B for both sentence and segment levels and prompted Llama 3-70B.
- Google T5: Fine-tuned for segment-level extraction.
- CRF and LSTM: Implemented for word-level key fact extraction.

# Evaluation
<a id="evaluation"></a>

The performance of the models was evaluated using various metrics:

- F1 Score: Used for sentence and word-level evaluation.
- ROUGE Score: Used for segment-level evaluation.

The evaluation results demonstrated that LLMs generally outperformed traditional rule-based methods due to being context-aware, particularly at the sentence and segment levels.

# Contributions
<a id="contributions"></a>

This research contributes to the field of computational linguistics by:

- Providing a comprehensive evaluation of LLMs at different levels of granularity.
- Demonstrating the effectiveness of fine-tuning and prompting LLMs for specific tasks.

# Future Work
<a id="future-work"></a>

Future directions for this project include:

- Expanding the dataset to include a wider variety of subjects and writing styles.
- Exploring advanced prompting techniques, such as Chain of Thought (CoT) and Knowledgeable Prompt-Tuning (KPT).
- Enhancing word-level extraction models by incorporating BiLSTM and predefined embeddings like Glove or ELMo.
