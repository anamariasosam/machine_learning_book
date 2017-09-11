# Aprendizaje de máquina

Se divide en dos grandes áreas:
1. **Aprendizaje supervisado**:
Se entrena un clasificador para identificar la etiqueta de un elemento nuevo. Las entradas para este modelo son: $$\mathbf{X}$$ la matriz de datos de dimension $$n\times p$$, donde $$n$$ es el numero de observaciones y $$p$$ es el numero de caracteristicas, y el conjunto de etiquetas $$C=[c_1, c_2, \ldots, c_k]$$, donde $$k$$ es el numero de clases

2. **Aprendizaje no supervisado**:
Se intenta agrupar el conjunto de datos, de tal forma que la separción entre los grupos sea la más conveniente. En este caso la entrada va a estar dado solo por la matriz de datos $$\mathbf{X}$$, definida por:

$$\mathbf{X} = \left[\begin{array}{cccc}
x_{11} & x_{12} & \ldots & x_{1p}\\
x_{21} & x_{22} & \ldots & x_{2p}\\
\vdots& &\ldots &\vdots \\
x_{n1} & x_{n2} & \ldots & x_{np}\\
\end{array}\right]$$

## Etapas modelo ML:

1. *Adquisición de datos*
2. *Acondicionamiento de los datos, tambien llamado preprocesamientos (filtrado y remoción de artefactos)*
3. *Caracterización*
4. ***Preprocesamiento de las caracteristicas***
5. *Reducción de dimensión*
6. ***Aplicación del modelo ML***
7. ***Analisis de resultado***
