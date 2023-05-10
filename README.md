# Text_Mining_On_Movie_Data

### Énoncé :
Le jeu de données fourni pour cet exercice s'appelle "Movie Data". Il
contient 50 000 lignes représentant des avis sur des films et des séries TV.
Chaque ligne se compose de deux colonnes : "review", contenant un avis
écrit en anglais scrappé sur un site spécialisé, et "sentiment", représentant
le label de chaque avis, c'est-à-dire s'il est positif ou négatif. L'objectif de
cet exercice sera alors de développer un modèle de classification de texte.

### Requirements
```bash
pip install numpy pandas matplotlib scikit-learn keras tensorflow keras-tcn mega.py
or from notebook
!pip install numpy pandas matplotlib scikit-learn keras tensorflow keras-tcn mega.py
```

### Code :

<a target="_blank" href="https://colab.research.google.com/github/pthavarasa/Text_Mining_On_Movie_Data/blob/main/Classification_de_texte.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>

### résultats
| Model | Accuracy | precision | recall | f1-score |
| :- | -: | -: | -: | -: |
| RNN | 90 | 90 | 90 | 90
| RNN Word2Vec | 90 | 90 | 90| 90
| Conv1D | 90 | 90 | 90 | 90
| TCN | 87 | 87 | 88 | 87

### Méthode de prédiction
Pour utiliser que la méthode de prédiction, suivre les étapes suivants :

1. Téléchargez et installez les packages et leurs dépendances. (bloc 3.1)
2. Importation des bibliothèques et modules nécessaires. (bloc 3.2)
3. Exécuter la cellule contient la login MEGA une fois que l'identifiant est remplie. (bloc 3.2)

Si vous n'ête pas conserné par les personnes qui ont eu l'identifiant partager, télecherger les models + tokenizer manuellement et importer sur colab.

* `sentiment_analysis_tokenizer.pickle` : https://mega.nz/file/ENdnhBgT#a74HxrLVK99mPb-_Wd9lq0B49s7qMb64meQ4l4l2VJ8
* `sentiment_analysis_rnn.h5` : https://mega.nz/file/tBcgkDYC#dtzHJWUTD6z0CgXF-qV4zDclo5HolbOKCLIysc294W4
* `sentiment_analysis_rnn_w2v.h5` : https://mega.nz/file/cQU0XYga#kRDDqQouOGGArRdYIE6ICxLI7G10kwh1UyDIP6EJsIc
* `sentiment_analysis_conv.h5` : https://mega.nz/file/xE9kTRwT#G76lwf9a22GRRcxljdbuvcrKGA0RMvu34cRaiKZjJ-I
* `sentiment_analysis_tcn.h5` : https://mega.nz/file/MEEnSIQS#a_7mscglYUh-Y_dBcGzxrEDlXr4s3oX9B-xAPvasPIQ

### Les techniques
- Nettoyage des données
  - Suppression des balises HTML à l'aide de l'expression regex.
  - Suppression des hashtags à l'aide de l'expression regex.
  - Suppression des mentions à l'aide de l'expression regex.
  - Suppression d'URL à l'aide d'une expression regex.
  - Conversion de toutes les lettres en minuscules.
  - Suppression de tous les caractères non alphabétiques (y compris la ponctuation et les chiffres) du texte.
  - Suppression stopword
  - Stemming
- Modèles
  - RNN
  - RNN Word2Vec
  - CNN
  - TCN
- Métrique
  - Accuracy
  - Precision
  - Recall
  - F1 score

### Source
* https://towardsdatascience.com/text-analysis-feature-engineering-with-nlp-502d6ea9225d?gi=6fdd856ca3bd
* https://towardsdatascience.com/a-beginners-guide-on-sentiment-analysis-with-rnn-9e100627c02e
* https://towardsdatascience.com/text-classification-with-nlp-tf-idf-vs-word2vec-vs-bert-41ff868d1794
* https://towardsdatascience.com/word-embedding-techniques-word2vec-and-tf-idf-explained-c5d02e34d08
* https://towardsdatascience.com/natural-language-processing-feature-engineering-using-tf-idf-e8b9d00e7e76
