# Kaggle-Specific Question-Answering Model

## Overview
This project leverages a pre-trained transformer model, specifically the Google Open-source Gemma LLM with 7 billion parameters, to enhance user experience on the Kaggle platform. By providing prompt and accurate responses to user inquiries, the project aims to streamline the process of searching for information and reduce the need for contacting support.

## Motivation
Since the introduction of ChatGPT in late 2022, the use of large language models (LLMs) for question-answering tasks has seen a significant increase, thanks to their impressive general question-answering capabilities. However, LLMs are not inherently equipped with specific knowledge in niche domains such as Kaggle, which often leads to inefficiencies in providing accurate answers to domain-specific queries.

## Solution
To overcome the limitations of generic LLMs, we employed a technique known as quantized low-rank adaptation (QLoRA) to fine-tune the Gemma LLM. This approach enables the model to adapt to the Kaggle-specific context using a synthetic dataset created from scraped Kaggle data.

## Challenges
Despite its successes, the fine-tuned model occasionally produces "hallucinations" — responses based more on the model's pre-trained context rather than the specific data it was trained on. Additionally, the model may default back to its general knowledge base when presented with vague questions or insufficient context.

## Implementation Details
- **Model Used:** Google Open-source Gemma LLM (7 billion parameters)
- **Technique:** Quantized Low-Rank Adaptation (QLoRA)
- **Training Environment:** Single GPU setup
- **Dataset:** Custom, Kaggle-specific synthetic dataset generated from scraped data.

## Findings
Our findings indicate that while the model successfully acquires domain-specific knowledge, there is still room for improvement in terms of reducing hallucinations and ensuring the model consistently applies its trained knowledge.

## How to Use
The notebook is provided [here](https://github.com/krittaprot/kaggle-gemma-peft/blob/main/QLoRA_Fine_Tuning_Gemma_Kaggle_Assistant.ipynb).
Download the dataset from this [link](https://github.com/krittaprot/kaggle-gemma-peft/tree/main/dataset) and upload to the content section of the colab storage for usage.

## Contributions
We welcome contributions from the community to enhance the model's performance and expand its applicability. Please refer to the contributing guidelines before making a submission.

## Authors
- Krittaprot Tangkittikun
- Kevin Simon Ireri Kori
- James Mbugua Mungai

## License
This project is released under the MIT License, which allows for liberal use and modification of the software.

## Acknowledgements
We would like to acknowledge the contributions of the open-source community and the developers of the Gemma LLM for making this project possible.

## Footnotes
- ChatGPT was launched by OpenAI and is accessible at [chat.openai.com](chat.openai.com).
