# Team Precog-LTRC-IIITH at GermEval 2021

Codes for our submission for the sub-tasks of the Germeval 2021 shared task on the Identification of Toxic, Engaging, and Fact-Claiming Comments.
The system we use is an ensemble of state-of-the-art pretrained models finetuned with engineered features. We show how feature engineering and data augmentation can be helpful when training data is less.

## Installing

We recommend using a virtual environment and running the following to install all the requirements

```bash
pip install -r requirements.txt
```

For faster training times using Tensorflow we recommending using the GPU. [Instructions](https://www.tensorflow.org/install/gpu)

## Reproducing the Results

### Preparing the Data

- Download the train and test data from the shared task website
- Copy them as `test.csv` and `train.csv` to `data` directory.
- To generate the augmented dataset as well as train and test dataset with features that we describe in our systems paper run the jupyter notebooks in `misc` directory.

### Running the models

- Download the FastText and Glove Embeddings that linked in external sources.
- Run the jupter notebooks in `models` directory
  - We recommend using [papermill](https://papermill.readthedocs.io/en/latest/) and running the training and predictions on a server in a batch job as the computations are heavy and long.
- Ensemble the outputs of these models.

### External Data Sources mentioned in the systems paper and used in this Repo

- [Emoji-list](https://bit.ly/3wtom8E)
- [FTRClassifier](https://bit.ly/3xER8Vk)
- [German-Verbs-Database](https://bit.ly/3i1BDzZ)

### Downloads

- [german glove embeddings by deepset.ai](https://bit.ly/3xwE58a)
- [german FastText embeddings](https://dl.fbaipublicfiles.com/fasttext/vectors-crawl/cc.de.300.vec.gz)

### Other links

- [Feature Engineering Notebooks and Visualisations on Google Colab](https://drive.google.com/drive/folders/1wG45ihqArFk81PHMBcbB-rirJH1zkwMz?usp=sharing)
