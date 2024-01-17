# Vietnamese Fake News Detection Based on Tokenization from Pre-trained Models and Word Embeddings BiLSTM Model


Detecting fake news on social media is a critical task to ensure information integrity. While there are several 
studies about fake news detection on English information, Vietnamese fake news detection remains limited.

In this research, we propose an approach for Vietnamese fake news using **pre-trained models forward tokenization** combined with word embedding inside 2 layers **Bidirectional Long Short Term Memory Network**.
Our proposed model is trained and evaluated on the dataset of Reliable Intelligence Identification on Vietnamese SNSs (ReINTEL), which contains nearly 10000 examples with labels.
Our experiments on the dataset demonstrate promising results with an accuracy of 0.9583 and an F1 score of 0.8684 using word tokenization from the Bartpho model, 
demonstrating our model’s effectiveness in detecting false news articles in Vietnamese.

## Table of Contents

- [Installation](#installation)
- [Data source](#datasource)
- [Contributing](#contributing)
## Installation

To get started with the project, you can follow these steps:

To use this project, you'll need to clone the repository. You can do this using Git:

```bash
git clone https://github.com/Akirahai/ECG_VISHC_Project.git
```

Next, make sure to install the necessary dependencies. You can create a Python virtual environment and install the requirements:

```bash
cd Massp_Fake-news-detection
pip install -r requirements.txt
```

## Data Source



For our research on Vietnamese fake news detection, we utilized the [ReINTEL 2020](https://aclanthology.org/2020.vlsp-1.16.pdf) dataset,
which was collected for a period of two months, from August to October 2020.
The dataset comprises a total of 9713 items, including both news articles and social media posts. These examples were collected from various sources, primarily from social media platforms (SNSs) and Vietnamese newspapers. The social media posts were retrieved
from news groups and key opinion leaders (KOLs), while the newspaper articles reported on
deleted fake news posts to ensure their inclusion.

The data covers a wide range of domains, such as entertainment, sports, finance, healthcare,
and the Covid-19 pandemic. During the data collection period, Vietnam experienced a significant surge in Covid-19 cases, leading to an ’infodemic’ with the rapid spread of misleading
information, particularly on social media platforms. This time frame, coupled with the
diversity of domains covered, makes the dataset highly suitable for training and evaluating
our proposed fake news detection model.

It is important to note that the [ReINTEL 2020](https://aclanthology.org/2020.vlsp-1.16.pdf) dataset by Le et al. is publicly available and was not
collected directly by us. However, we selected it as the basis for our research due to its
comprehensive coverage, balanced class distribution, and real-world relevance.

## Contributing

Our proposed model achieved an impressive accuracy of 95.83% on the test set for classifying Vietnamese news as real or fake. Surpassing 90% accuracy demonstrates that deep
learning approaches like LSTMs are highly effective for this task when provided with sufficient training data.

Several factors contributed to the high accuracy:
* The bidirectional LSTM architecture was able to build robust sequential representations of the tokenized articles by processing both past and future context. 
* Pre-training the BERT word embeddings on a large corpus enabled the model to leverage semantic and syntactic representations tailored for the Vietnamese language.
* The large labeled dataset used for training was critical for the model to learn the nuanced patterns that distinguish fabricated from factual stories.


