# Codificación de Etiquetas

El usuario ingresa primero las etiquetas, es decir: 'perro', 'gato', 'pajaro'. Luego ingresa todos los datos para armar el array y luego lo convierto en valores numericos.

```python
def diccionario(etiquetas):
    keys = etiquetas.split(',')
    values = list(range(len(keys)))
    hash = {k:v for k, v in zip(keys, values)}

    return hash

def codificacion(datos, hash):
    data = datos.split(',')

    key_number = list()
    for i in range(len(data)):
        key_number.append(hash[data[i]])

    return key_number

etiquetas = input('Ingresa las etiquetas separadas por coma ')
hash = diccionario(etiquetas)

datos = input('Ingresa las etiquetas separadas por coma ')
key_number = codificacion(datos, hash)

print(key_number)

```
