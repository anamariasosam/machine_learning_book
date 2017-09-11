# Binarización

Convertir las caracteristicas en variables booleanas. Se debe fijar un umbral $$\gamma$$ para la binarización de los datos

## Método de binarización
```python
def binarizacion(X, gamma) :
    filas = np.shape(X)[0]
    columnas = np.shape(X)[1]

    for i in range(filas) :
        for j in range(columnas) :
            X[i][j] = 1 if X[i][j] >= gamma else 0
    return X
```

## LLamámos el método
```python
gamma = float(input('Ingrese el valor de gamma'))
datos_binarizados = binarizacion(X,gamma)

print(datos_binarizados)
```
