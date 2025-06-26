# Farmacovigilancia: Análisis de efectos adversos de un ensayo clínico Fase III

Este es un proyecto de análisis de datos de efectos adversos de un ensayo clínico fase III realizado por la farmacéutica GSK utilizando librerías de python como seaborn, matplotlib, sklearn y scipy.stats; los datos se obtuvieron del repositorio  de datos del Departamento de bioestadistica de la universidad de Vanderbilt (https://hbiostat.org/data/).

## ¿Qué se realizó?

* Se hizo un análisis exploratorio, se graficaron boxenplots y funciones de distribución acumuladas empíricas para ver patrones en los laboratorios clínicos de ambos grupos
* Se analizaron los efectos adversos más comunes y se realizaron pruebas de hipótesis, siempre verificando la disrtibución de los datos
* Se realizó Clustering aglomerativo para agrupar efectos adversos y laboratorios clínicos
* Utilizando algoritmos de bagging se trató de desarrollar un modelo que logre predecir la aparición de la exacerbación de la Enfermedad Pulmonar obstructiva crónica (coad en inglés).
  
## ¿Qué se concluye?

* Existe una ligera diferencia de edad entre los grupos y el conteo plaquetario en el grupo Placebo fue menor
* La mayoría de distribuciones de laboratorios clínicos no cumplen con normalidad por lo que son necesarias pruebas no paramétricas
* La exacerbación de 'coad' está relacionada, paradójicamente, con el grupo Placebo
* El clustering de laboratorios clínicos dejo ver clásicas relaciones de biomarcadores hepáticos, renales y hematológicos; el clustering de efectos adversos dejo ver una relacion entre diharrea, dolor abdominal y nausea
* Si bien la precision y sensibilidad de los algoritmos de RandomForest y XGboost no fue óptimo, se observa el uso de variables como frecuencia respiratoria, f. cardiaca, conteo plaquetario y bmi en la predicción de la exacerbación de 'coad'

## Bibliografía
* Clauset, A., C. R. Shalizi, and M. E. J. Newman. 2009. “Power-Law Distributions in Empirical Data.” SIAM Review 51: 661–703.
* Géron, A. (2019). Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow: Concepts, Tools, and Techniques to Build 
  Intelligent Systems (2nd ed.). O’Reilly Media. ISBN 978-1-4920-3264-9
* Qian Y, Cai C, Sun M, Lv D, Zhao Y. Analyses of Factors Associated with Acute Exacerbations of Chronic Obstructive Pulmonary Disease: A 
  Review. Int J Chron Obstruct Pulmon Dis. 2023 Nov 24;18:2707-2723. doi: 10.2147/COPD.S433183. PMID: 38034468; PMCID: PMC10683659.
* https://fastercapital.com/es/contenido/Wilcoxon-vs--Mann-Whitney-U-Prueba--cual-elegir.html
* https://www.ibm.com/mx-es/think/topics/random-forest
* https://www.ibm.com/think/topics/xgboost
* https://www.ibm.com/es-es/think/topics/hierarchical-clustering

*
*
