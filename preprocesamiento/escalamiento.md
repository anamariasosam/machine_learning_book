# Escalamiento
Medir con la misma *regla* todas las caracteristicas a todas las caracteristicas,para ello se realiza la siguiente operacion:


$$\frac{\mathbf{X}-min(\mathbf{X})}{max(\mathbf{X}) - min(\mathbf{X})},$$

## Método de escalamiento
```python
def escalamiento(X):
    X = X - X.min(axis=0)
    X = X/(X.max(axis=0) - X.min(axis=0))

    return X

```

## Llamámos el método

```python
datos_escalados = escalamiento(X)
print(datos_escalados)
```
