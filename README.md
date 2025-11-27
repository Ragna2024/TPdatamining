1.Description claire des étapes suivies. 
Le fichier Mall_Customers.csv est tout d'abord importé et étudié pour mieux saisir sa structure ainsi que les variables qu'il contient. 
Ensuite, nous analysons ses données afin de détecter d'éventuelles valeurs manquantes. Puisque toutes les informations sont complètes, aucune mesure corrective n'est nécessaire. 
Par la suite, les distributions des variables sont examinées à l'aide d'histogrammes et de statistiques descriptives, permettant d'avoir un aperçu clair de leurs répartitions. 
Pour effectuer cet segmentation, trois variables clés sont sélectionnées : Age, Annual Income (k$) et Spending Score (1-100). Ces dernières sont choisies car elles reflètent le profil démographique, le pouvoir d'achat et le comportement des clients. 
Afin de les rendre comparables, une normalisation est réalisée avec StandardScaler pour les standardiser sur une échelle uniforme pour pouvoir par la suite utiliser un modèle K-Means. 

2.Justifications des choix (k, variables, interprétations). 
Tout d’abord, nous analysons les relations entre les variables choisies afin de mieux appréhender la structure du dataset. 
Pour cela, des visualisations comme les scatter plots ou encore une heatmap de corrélation sont utilisées afin d’examiner les interactions entre des variables telles que l’âge, le revenu annuel et le score de dépense. 
De plus, la matrice de corrélation, en particulier, permet d’identifier les relations fortes ou faibles entre ces différentes dimensions. Ces représentations graphiques offrent également la possibilité de détecter des regroupements naturels au sein des données avant même de recourir à l’algorithme K-Means. 
Par exemple, des zones de densité accrue visibles dans les scatter plots peuvent suggérer l’existence de segments distincts. 
Sur la base de ces observations, il est possible d’émettre une première hypothèse quant au nombre potentiel de clusters, estimé ici entre 4 et 6 groupes, ce qui servira à orienter la sélection du paramètre k. 


3.Visualisations propres et lisibles. 
Distribution des variables
Relation entre les variables
Visualisation de la méthode du Coude (pour choisir le nombre optimal de cluster)
Visualisations des cluster en 2D et 3D

4.Analyse critique des résultats. 

L’utilisation du K-Means permet de distinguer clairement plusieurs groupes de clients aux caractéristiques variées. 
Les visualisations en 2D et 3D révèlent une séparation plutôt distincte entre certains clusters, notamment ceux regroupant les clients à revenus élevés et ceux ayant des scores de dépenses importants. 
Toutefois, cet algorithme présente certaines limites. 
D’une part, K-Means repose sur l’hypothèse que les clusters sont sphériques et de taille comparable, ce qui ne reflète pas toujours la réalité des données et peut entraîner une segmentation moins précise pour des groupes plus hétérogènes. 
D’autre part, déterminer le nombre optimal de clusters reste une décision subjective : bien que des techniques comme la méthode du coude ou le silhouette score soient utiles, elles n’assurent pas nécessairement une pertinence parfaite en termes d’applications métier. 
Par ailleurs, il est possible d’observer un léger chevauchement entre certains clusters dans les visualisations, ce qui suggère une structure des données peut-être plus complexe qu’un simple regroupement en k entités. 
En conséquence, il pourrait être judicieux de compléter cette analyse avec des approches alternatives de clustering, telles que DBSCAN ou GMM, ou encore d’incorporer davantage de variables afin d’assurer une segmentation plus robuste et pertinente. 


