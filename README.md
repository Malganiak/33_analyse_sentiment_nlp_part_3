# 33_analyse_sentiment_nlp_part_3

Introduction au Traitement Automatique du Langage Naturel (TALN) : Analyse de Sentiment - Partie Trois

Dans cette section, nous aborderons les techniques avancées de "Transfer Learning" dans le domaine du Traitement Automatique du Langage Naturel (TALN), en mettant particulièrement l'accent sur leur application dans l'analyse de sentiments.

Ressources :

Universal Language Model Fine-tuning for Text Classification
TensorFlow Hub
Universal Sentence Encoder
TensorFlow Datasets
Contexte du Projet :
La section précédente a présenté les concepts fondamentaux de la vectorisation de mots (Word Embedding) dans le contexte du TALN, en se concentrant spécifiquement sur son application à l'analyse de sentiments à partir de la base de données IMDb. Cependant, malgré ces fondamentaux, l'impact sur la performance reste relativement limité. Avant la publication de l'article "Universal Language Model Fine-Tuning ULMFiT", le pré-entrainement en TALN était principalement basé sur l'utilisation de "Word Embeddings". L'article a marqué le début d'une nouvelle ère en introduisant l'utilisation de modèles de langage préentrainés comme norme pour le "Transfer Learning" en TALN. Ainsi, l'objectif de cette section est de combiner des couches "embedding" préentrainées de modèles de langage avec un perceptron multicouches et d'effectuer un "fine-tuning" sur la base de données IMDb. Plus précisément, nous envisageons de coupler le modèle de langage "Universal Sentence Encoder" fourni par Google via TensorFlow Hub avec un perceptron multicouche pour réaliser l'analyse de sentiment.

Quelques conseils pratiques :

Entraîner le modèle sur les données textuelles fournies, par exemple, par la bibliothèque "tensorflow_datasets".
Privilégier l'utilisation de minibatch.
Limiter le nombre d'epochs à 10.
Utiliser l'instruction "os.environ["TFHUB_CACHE_DIR"] = "my_tfhub_cache" pour sauvegarder le modèle localement. Étant donné que le modèle de langage a une taille d'environ 1 Go, la sauvegarde locale évitera de le télécharger à chaque relance du notebook.
Livrables :
Un Jupyter Notebook.

Critères de Performance :
Les critères d'évaluation incluent la clarté et la qualité du code Python dans le notebook.
