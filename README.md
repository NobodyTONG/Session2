## Project Name: Improving Product Quality and Customer Satisfaction Using Insurance Complaint Analysis and SpaCy Classification Models
The project analyzed several insurance complaint issues using visualization techniques and developed models to categorize complaints and predict the claim outcome. With a manually labelled dataset of 167 records, the study fine-tuned a pre-trained Bidirectional Encoder Representations from Transformers (BERT) Model, achieving 91.2% accuracy in classifying complaint text. To obtain better binary decision model, the project compares Logistic Regression Classification Model and SpaCy Model under the same dataset. It found that the SpaCy Model performs especially excellent in 'precision' indicators, with a recall of 98.1% and a similar accuracy of 84.9%.

The study provides valuable recommendations for Simply Business to focus on improving insurance regulations and refining the clauses on compensation amounts as they are key strategies to reduce future disputes. With an accurate binary decision model, Simply Business can previously manage on handling complaints, helping to prevent the costs associated with uncertain compensation amounts.


## Content
- [Required Package Version] 
- [Dataset] (Can be downloaded from )
- [Model Evaluation] indicators: Accuracy, Precision, Recall, F1-score


## Required Package Version
pypdf==4.2.0, pandas==2.2.2, torch==2.1.2+cpu, numpy==1.26.4, transformers==4.42.3, datasets==2.20.0, sklearn-pandas==2.2.0, wandb==0.17.4, matplotlib==3.7.5, seaborn==0.12.2, wordcloud==1.9.3, spacy==3.7.5, nltk==3.2.4, yake==0.4.8


## Dataset
The API command of dataset is 'kaggle datasets download -d houhuantong/half-year-data' OR you can search 'HOU Huantong' in Kaggle page and find 'half_year_data' dataset.

- 'half-year-date/': 
	  - 167labelled.csv
	  - metadata.csv
	  - 'ICMweights/'
	    - 'weights-0.91/'
	      - 'model/'
	        - 'config.json'
	        - 'model.safetensors'
	      - 'tokenizer/'
	        - 'special_tokens_map.json'
	        - 'tokenizer_config.json'
	        - 'vocab.txt'
	  - 'Spacyweights/'
	    - 'Spacy/'
	      - 'textcat/'
	        - 'cfg'
	        - 'model'
	      - 'vocab/'
	        - 'config.cfg'
	        - 'meta.json'
	        - 'tokenizer'
	  - 'decisions/'
	    - 'decisions/'
	      - 'DRN-4020987.pdf'
	      ... (3212 pdf files)


## Model Evaluation
| Model                           | Train Accuracy | Precision | Recall | F1-Score |
|---------------------------------|----------------|-----------|--------|----------|
| Insurance Classification Model  | 0.912          | 0.872     | 0.912  | 0.888    |


| Model                              | Train Accuracy | Test Accuracy | Precision | Recall | F1-Score |
|------------------------------------|----------------|---------------|-----------|--------|----------|
| Logistic Regression Classification | 0.89           | 0.84          | 0.89      | 0.89   | 0.89     |
| SpaCy Classification               | 0.849          | 0.792         | 0.770     | 0.981  | 0.861    |

