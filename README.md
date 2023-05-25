## medias_QC

Projet de ML pour classer les médias québécois selon leur tendance gauche/droite

### Étapes

Le classement d'un texte sur le spectre politique de gauche à droite est une tâche complexe, mais certainement réalisable avec SpaCy et d'autres outils de machine learning. Pour ce faire, vous auriez besoin de créer un modèle de classification de texte. Voici les étapes générales pour aborder ce problème :

- Collecte de données : Avant de pouvoir entraîner un modèle pour classer les textes politiques, vous aurez besoin d'un grand ensemble de textes étiquetés avec leur orientation politique. Ces textes peuvent provenir de différentes sources, comme des articles de presse, des transcriptions de discours politiques, des publications sur les réseaux sociaux, etc. Le plus important est que chaque texte soit étiqueté avec son orientation politique (par exemple, "gauche", "centre", "droite").

- Prétraitement du texte : Une fois que vous avez collecté vos données, vous devrez les prétraiter pour les préparer à être utilisées dans un modèle de machine learning. Cela peut inclure des tâches comme la tokenisation (diviser le texte en mots individuels), la lemmatisation (réduire les mots à leur forme de base), la suppression des mots vides (des mots comme "et", "la", "à", qui n'apportent pas beaucoup d'information), et d'autres techniques de nettoyage et de normalisation du texte. Vous pouvez utiliser SpaCy pour effectuer ces tâches de prétraitement.

- Extraction des caractéristiques : Pour pouvoir utiliser vos textes dans un modèle de machine learning, vous devrez transformer chaque texte en un ensemble de caractéristiques numériques. Une approche commune consiste à utiliser le modèle de "sac de mots" (bag-of-words) ou le TF-IDF (Term Frequency-Inverse Document Frequency). Une autre approche consiste à utiliser des vecteurs de mots, comme ceux fournis par Word2Vec, FastText ou GloVe. Vous pouvez également utiliser le Doc2Vec, qui génère un vecteur pour un document entier. SpaCy peut vous aider à extraire ces types de caractéristiques.

- Entraînement du modèle : Une fois que vous avez transformé vos textes en caractéristiques numériques, vous pouvez les utiliser pour entraîner un modèle de classification. Il existe de nombreux types de modèles que vous pourriez utiliser, comme la régression logistique, les machines à vecteurs de support (SVM), les arbres de décision, les forêts aléatoires, les réseaux de neurones, etc. Vous pouvez utiliser des bibliothèques comme Scikit-learn, TensorFlow ou PyTorch pour entraîner ces modèles.

- Évaluation du modèle : Après avoir entraîné votre modèle, vous devrez l'évaluer pour voir à quel point il est précis. Vous pouvez le faire en utilisant une partie de vos données que vous avez réservée pour le test (c'est-à-dire que vous ne l'avez pas utilisée pour l'entraînement). Vous pourriez également utiliser la validation croisée pour obtenir une évaluation plus robuste.

- Application du modèle : Une fois que vous êtes satisfait de la performance de votre modèle, vous pouvez l'utiliser pour classer de nouveaux textes selon leur orientation politique. Vous devrez prétraiter ces nouveaux textes et extraire leurs caractéristiques de la même manière que vous l'avez fait pour les textes d'entraînement. Ensuite, vous pouvez passer ces caractéristiques à votre modèle, qui générera une prédiction de l'orientation politique du texte.

### Taille des corpus gauche/droite/centre

La taille de l'ensemble de données nécessaire pour l'entraînement d'un modèle de machine learning dépend de plusieurs facteurs, dont la complexité de la tâche, la variété du langage utilisé dans les textes, la complexité du modèle utilisé, et ainsi de suite.

En règle générale,  pour les tâches classification de texte, on peut dire que "plus c'est mieux". Des ensembles de données plus grands ont tendance à permettre aux modèles d'apprendre des modèles plus précis et plus généraux. Cependant, l'entraînement sur de très grands ensembles de données peut également nécessiter plus de ressources informatiques et plus de temps.

Pour un problème comme le classement des textes sur le spectre politique, où le langage peut être très varié et la distinction entre les classes peut être subtile, un ensemble de données de taille moyenne à grande serait probablement nécessaire. Par exemple, vous pourriez commencer avec des dizaines de milliers de textes pour chaque classe (gauche, centre, droite) si possible.

Cependant, il est important de noter que la taille de l'ensemble de données n'est pas le seul facteur important. La qualité des données est également cruciale. Vous devez vous assurer que les textes sont bien étiquetés et qu'ils sont représentatifs de la variété des textes que vous voulez que votre modèle soit capable de classer.

Enfin, il peut être utile de commencer avec un ensemble de données plus petit et de tester une version plus simple de votre modèle pour voir comment il fonctionne. Cela peut vous aider à identifier les problèmes potentiels plus tôt et à décider si vous avez besoin de collecter plus de données ou de faire des ajustements à votre modèle ou à votre processus de prétraitement.
