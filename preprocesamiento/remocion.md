# Remoción de la media

Eliminar la tendencia de los datos. La operación que se realiza sobre la matriz de datos es la siguiente:

$$\frac{\mathbf{X}-\mathbf{\hat{X}}}{\sigma_{\mathbf{X}}},$$

donde $$\mathbf{\hat{X}}$$ es la media y $${\sigma_{\mathbf{X}}}$$ es la desviación

## Método de remoción
```python
def remocion(X):
    X = X - X.mean(axis=0)
    X = X/X.std(axis=0)

    return X
```

## LLamámos el método
```python
  datos_centralizados = remocion(X)
  media = datos_centralizados.mean(axis=0)
  print('La media de las caracteristicas es', media)
  desviacion = datos_centralizados.std(axis=0)
  print('La desviacion de las caracteristicas es', desviacion)
```
