## Normalización L1
Es posible eliminar la influencia de los valores atípicos (*outliers*). La idea de esta normalización es que la suma del valor absoluto sea unitaria. i.e:

$$ \sum_{j=1}^{p}||x_{ij}||=1, \quad\quad \forall i=1, \ldots, n$$

## Método de normalización L1
```python
def normalizacion_uno(X):
    norm = LA.norm(X, ord=1, axis=1)

    filas = np.shape(X)[0]
    columnas = np.shape(X)[1]

    for i in range(filas) :
        X[i][:] =  X[i][:] / norm[i]
    return X

```

## Llamámos el método

```python
datos_normalizados = normalizacion_uno(X)
print(datos_normalizados)
```
