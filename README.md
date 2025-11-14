
# Analyse de la relation entre Federal Funds Futures et taux effectif

L’objectif est d’étudier le lien entre les Federal Funds Futures et le taux effectif des Fed Funds (EFFR / FEDFUNDS), et d’évaluer dans quelle mesure l’information contenue dans les futures permet d’anticiper les hausses de taux de la Fed.

Dans une première partie, nous :

- chargeons et mettons en forme les séries historiques (EFFR et Federal Funds Futures) ;

- construisons le taux implicite à partir des contrats futures ;

- fusionnons les séries pour obtenir, à chaque date, le couple (taux implicite, taux effectif) ;

- analysons graphiquement la dynamique des deux séries et la différence (spread) entre taux implicite et taux effectif.

Dans une seconde partie, nous construisons une variable cible binaire indiquant si le taux FEDFUNDS augmente au pas de temps suivant, et nous utilisons ce spread (ainsi que ses retards et éventuellement d’autres variables, comme la volatilité) comme features dans un modèle de régression logistique.
Nous comparons ensuite deux approches d’évaluation :

- un schéma walk-forward avec ré-estimation récursive (évaluation hors-échantillon, plus réaliste) ;

- un entraînement global sur toute l’histoire disponible (évaluation in-sample, plus optimiste).

L’objectif n’est pas de proposer un modèle de trading complet, mais de montrer, de manière pédagogique, comment exploiter les Federal Funds Futures pour estimer la probabilité d’une hausse de taux et comparer différents cadres d’évaluation prédictive.

On propose deux notebooks: `preliminary_model` (la modélisation introductive) et `main_model` (qui permet de maximiser les métriques)


Afin d'accéder aux travaux: 

```bash
git clone https://github.com/OmarELMAMOUNE/ML-FINANCE-ENSAE.git

```

Afin d'installer les packages:

```bash
cd ML-FINANCE-ENSAE
pip install -r requirements.txt

```





Les données utilisées:

- https://fred.stlouisfed.org/series/FEDFUNDS
  
- https://www.cmegroup.com/markets/interest-rates/stirs/30-day-federal-fund.settlements.html

- https://fred.stlouisfed.org/series/PCEPI

- https://fred.stlouisfed.org/series/PAYEMS

- https://fred.stlouisfed.org/series/GDP

- https://fred.stlouisfed.org/series/INDPRO

- https://fred.stlouisfed.org/series/CPIAUCSL
