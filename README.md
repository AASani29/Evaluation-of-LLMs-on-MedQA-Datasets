# Evaluation of LLMs on Medical QA Datasets

This repository contains notebooks for evaluating different Language Learning Models (LLMs) on medical question-answering tasks using the iCliniq dataset.

## Models Evaluated

- **GPT-4o**: OpenAI's advanced language model
- **GPT-3.5-turbo**: OpenAI's efficient language model  
- **Llama-3.2-1B-Instruct**: Meta's instruction-tuned model

## Setup Instructions

### 1. Environment Setup

First, set up your OpenAI API key as an environment variable:

#### Windows (PowerShell):
```powershell
$env:OPENAI_API_KEY="your-api-key-here"
```

#### Windows (Command Prompt):
```cmd
set OPENAI_API_KEY=your-api-key-here
```

#### Linux/Mac:
```bash
export OPENAI_API_KEY="your-api-key-here"
```

### 2. Install Dependencies

```bash
pip install openai nltk numpy transformers torch
```

### 3. Dataset

Ensure the `icliniqQAs.json` file is in the same directory as the notebooks.

## Notebooks

1. **Zero-Shot using gpt-4o.ipynb** - Evaluates GPT-4o on medical QA
2. **Zero-Shot using gpt-3.5-turbo.ipynb** - Evaluates GPT-3.5-turbo on medical QA
3. **Zero-Shot using Llama-3.2-1b-Instruct.ipynb** - Evaluates Llama-3.2-1B on medical QA

## Evaluation Metrics

- **BLEU Score**: Measures n-gram overlap between generated and reference answers
- **Word Overlap**: Percentage of words shared between responses
- **Medical Domain Relevance**: Frequency of medical terminology usage
- **Response Length Analysis**: Comparison of generated vs reference answer lengths

## Results

Results are automatically saved to JSON files:
- `gpt4o_medical_qa_results.json`
- `gpt35_turbo_medical_qa_results.json`
- `llama32_medical_qa_results.json`

## Security Note

- API keys are loaded from environment variables for security
- Never commit API keys directly to the repository
- The `.env` file is ignored by git to prevent accidental exposure

## Usage

1. Set your OpenAI API key as an environment variable
2. Open the desired notebook
3. Run all cells to perform the evaluation
4. Check the results in the generated JSON files

## Requirements

- Python 3.8+
- OpenAI API key
- Hugging Face account (for Llama models)
- Sufficient API credits for model inference
