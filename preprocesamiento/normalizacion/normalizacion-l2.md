## Normalización L2
Es posible hacer más notable la influencia de los valores atípicos (*outliers*). La idea de esta normalización es que la suma del valor absoluto al cuadrado sea unitaria i.e:

$$ \sum_{j=1}^{p}||x_{ij}||^2=1, \quad\quad \forall i=1, \ldots, n$$

## Método de normalización L2
```python
def normalizacion_dos(X):
    norm = LA.norm(X, ord=2, axis=1)

    filas = np.shape(X)[0]
    columnas = np.shape(X)[1]

    for i in range(filas) :
        for j in range(columnas) :
            X[i][j] =  X[i][j] / norm[i]
    return X

```

## Llamámos el método

```python
datos_normalizados = normalizacion_dos(X)
print(datos_normalizados)
```
