## Résultats

### 1. **Erreur Moyenne Quadratique (RMSE) : 7.899**

**RMSE** mesure la différence moyenne entre les valeurs prédites par le modèle et les valeurs réelles. Plus la valeur de l'erreur quadratique moyenne est petite, meilleur est le modèle.

- **Interprétation** :
  - Un **RMSE de 7.899** signifie qu'en moyenne, les prédictions du modèle s'écartent de la performance globale (`performance_index`) réelle d'environ **8** points.
  - Par exemple, si la performance globale réelle d'un étudiant est de **80**, la valeur de la performance prédite serait en moyenne dans la plage de **80 ± 7.899** (entre **72 - 88** approximativement).

---

### 2. **R-carré (R²) : 0.833**

**R²** indique à quel point le modèle explique la variance de la performance globale de l'étudiant. Il nous dit quelle proportion de la variance totale est expliquée par notre modèle.

- **Interprétation** :
  - Un **R² de 0.833** signifie que **83.3 %** de la variance de la preformance globale d'un étudiant peut être expliquée par les notes obtenues par cet individu lors des tests précédents (`previous_scores`). La valeur du R² (0.833) suggère que les scores obtenues par cet étudiant lors des tests précédents est un très bon prédicteur du de sa performance global.
  - Par example, si l'on prédit les scores d'examen avec les scores précédents, **83.3 %** de la variabilité des performances d'examen est expliquée par les scores précédents. Cela montre que les scores précédents d'un étudiant sont un déterminant majeur de la performance actuelle de cet étudiant.

---

### 3. **Erreur Absolue Moyenne (MAE) : 6.747**

**MAE** mesure la moyenne des erreurs absolues entre les valeurs prédites et réelles. Contrairement au RMSE, le MAE ne pénalise pas davantage les grandes erreurs, tandis que le RMSE donne plus de poids aux grandes erreurs.

- **Interprétation** :
  - Un **MAE de 6.747** signifie qu'en moyenne, les prédictions du modèle s'écartent d'environ **7** points de la performance globale réelle.
  - Par exemple, pour un indice de performance global réel de **80**, la valeur prédite serait en moyenne écartée de **±6.747** points, ce qui signifie que la valeur prédite pourrait varier entre **73.25 et 86.75**.

---

### 4. **Erreur Quadratique Moyenne (MSE) : 62.394**

**MSE** mesure la moyenne des différences au carré entre les valeurs prédites et réelles. Il pénalise davantage les grandes erreurs que le MAE en raison de l'élévation des résidus au carré, ce qui le rend sensible aux valeurs aberrantes.

- **Interprétation** :
  - **MSE = 62.394** signifie que l'erreur quadratique moyenne entre les valeurs prédites et réelles de la performance globale `performance_index` est de **62.394**.
  - Puisque le MSE est plus grand que le MAE, il reflète que les erreurs du modèle incluent certaines grandes erreurs.

---

### **Conclusion :**

Le modèle de régression linéaire fonctionne **bien** avec les scores précédents comme prédicteur de l'indice de performance, atteignant un R² de **0.833**. Cela signifie qu'environ **83%** de la variation de la performance globale d'un individu peut être expliquée par ses scores précédents, ce qui montre que ces derniers sont un bon prédicteur de la performance actuelle.

Les métriques d'erreur, comme l'**Erreur Quadratique Moyenne (RMSE)** de **7.899** et l'**Erreur Absolue Moyenne (MAE)** de **6.747**, indiquent que le modèle est relativement précis, avec des erreurs moyennes inférieures à 8 points. Cela suggère que les prédictions du modèle sont en moyenne proches de la réalité, bien qu'il reste encore quelques écarts à corriger.

Étant donné cette bonne performance, ce modèle pourrait être très utile pour prédire la performance des étudiants en fonction de leurs scores précédents. Cependant, pour améliorer encore la qualité des prédictions, il serait pertinent d'explorer l'ajout de nouvelles caractéristiques, telle que le nombre d'heures d'étude(`hours_studied`) qui pourraient enrichir le modèle et améliorer sa capacité à prédire l'indice de performance de manière plus précise.

### Sources utiles
MLlib (DataFrame-based) — PySpark 3.5.3 documentation. (n.d.). https://spark.apache.org/docs/latest/api/python/reference/pyspark.ml.html 

loading. . . | SAP Help Portal. (n.d.). https://help.sap.com/docs/SAP_PREDICTIVE_ANALYTICS/41d1a6d4e7574e32b815f1cc87c00f42/5e5198fd4afe4ae5b48fefe0d3161810.html

API reference — seaborn 0.13.2 documentation. (n.d.). https://seaborn.pydata.org/api.html

https://www.machinelearningplus.com/pyspark/pyspark-linear-regression/ 


