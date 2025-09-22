# Estadística de Divorcios 2023 - Regresión Logística  

## **Descripción**  
Este repositorio contiene el desarrollo de una tarea práctica utilizando la **Estadística de Divorcios 2023 (INEGI)**.  
El objetivo principal fue **predecir la duración legal del matrimonio (`dura_leg`)** mediante un modelo de **regresión logística**, aplicando técnicas de **binarización de variables, selección de características, validación cruzada y evaluación de métricas de clasificación**.  

## **Contenido del proyecto**  
- **Paso 1:** Binarización de `dura_leg` en `dura_leg_bin`.  
- **Paso 2:** División del dataset en entrenamiento (80%) y prueba (20%) manteniendo balance de clases.  
- **Paso 3:** Selección de características con ANOVA F-statistic y validación cruzada de la regresión logística.  
- **Paso 4:** Entrenamiento final y evaluación en el conjunto de prueba con matrices de confusión a distintos umbrales (0.3, 0.5, 0.7).  
- **Paso 5:** Gráfico de la curva ROC y reporte del AUC.  

## **Resultados principales**  
- La variable `dura_leg` se distribuyó en clases relativamente balanceadas: 55% clase 0 y 45% clase 1.  
- Las **5 variables seleccionadas** fueron: `edad_div1`, `edad_div2`, `hijos`, `pension_4.0`, `cus_hij`.  
- La **validación cruzada (CV=10)** de la regresión logística alcanzó una **exactitud promedio ≈ 0.84**, mostrando estabilidad en los diferentes folds.  
- En el conjunto de prueba:  
  - Con umbral **0.3**: sensibilidad 0.918 y especificidad 0.731.  
  - Con umbral **0.5**: sensibilidad 0.824 y especificidad 0.854 (mejor balance).  
  - Con umbral **0.7**: sensibilidad 0.694 y especificidad 0.923.  
- La **curva ROC** mostró un AUC = **0.92**, indicando un alto poder de discriminación del modelo.  

## **Archivos del repositorio**  
- [Notebook de la tarea en formato .ipynb](./ED_Divorcios2023_Notebook.ipynb)  
- [Reporte en formato .pdf](./ED_Divorcios2023_Reporte.pdf)  
- [Reporte en formato .html](./ED_Divorcios2023_Page.html)  
- [Base de datos CSV](./Estadisticas_divorcios_Mexico_2023_P1.csv)  
