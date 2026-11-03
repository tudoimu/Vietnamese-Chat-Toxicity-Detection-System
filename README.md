# Vietnamese Chat Toxicity Detection System

An open-source Natural Language Processing (NLP) classification model designed to detect, filter, and categorize toxic language in Vietnamese gaming communities and online chat environments.

## Project Overview
Toxic behavior and harassment are prevalent in competitive online gaming. This project aims to build a robust NLP pipeline to moderate Vietnamese chat logs. Instead of a simple binary classification, this system utilizes a nuanced 3-class categorization to differentiate between casual profanity and directed hate speech.

## Dataset & Labeling
The model is trained on a custom, diverse bilingual dataset comprising **60,000 - 80,000 chat logs**. 
* **Data Sources:** Real-world chat histories from competitive games (League of Legends, Valorant, CS:GO) augmented with Generative AI data to ensure edge-case coverage.
* **Labeling Architecture:** The dataset is strictly labeled into 3 categories to establish a nuanced baseline:
  * `0 : Clean` - Normal, non-toxic communication.
  * `1 : Offensive` - General profanity or casual toxic behavior without a specific target.
  * `2 : Hate Speech` - Directed insults, discrimination, or severe harassment towards individuals/groups.

## Model & Methodology
* **Environment:** Python 3, Google Colab.
* **Approach:** 
  1. Evaluated custom baseline architectures built from scratch.
  2. Fine-tuned the open-source **Detoxify** model (originally by UnitaryAI) to maximize predictive accuracy for the Vietnamese language context.

## Repository Structure
* `Vietnamese Chat Toxicity Detection System.ipynb`: The main Google Colab notebook containing data preprocessing, model training, and evaluation code.
* `LICENSE`: MIT License.

## Getting Started
To explore or run the model yourself:
1. Open the `Vietnamese Chat Toxicity Detection System.ipynb` file in this repository.
2. Click the **"Open in Colab"** badge (if configured) or download the file and upload it to your Google Colab environment.
3. Ensure your Colab runtime is set to **GPU** (T4 or higher) for faster training/inference.
4. Run the cells sequentially to install dependencies (`transformers`, `datasets`, etc.) and execute the pipeline.

## Future Work (Roadmap)
* [ ] Expand the dataset to include multi-label classification for highly specific toxicity (e.g., regional discrimination, racism).
* [ ] Scale the dataset for specialized edge cases (aiming for 20k-30k rows per specific sub-label).
* [ ] Deploy the trained model as a lightweight REST API for real-time game chat integration.

## License
This project is licensed under the [MIT License](LICENSE).
