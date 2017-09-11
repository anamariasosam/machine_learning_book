# Aprendizaje Supervisado
Con el fin de aplicar un modelo supervisado para la clasificación de datos, es necesario iniciar con la carga o adquisición de los datos,en nuestro caso será una matriz  $$\mathbf{X}$$  artificial:

$$\mathbf{X} = \left[\begin{array}{ccc}
5.1&-2.0&3.3\\
-1.2&7.8&-6.1 \\
3.9&0.4&2.1\\
7.3&-9.9&-4.5 \\
\end{array}\right]$$


### Creamos la matriz con los datos
A esta matriz le aplicaremos todos los métodos de preprocesamiento
```python
import numpy as np
from numpy import linalg as LA

X = np.array([[5.1,-2.9,3.3],[-1.2,7.8,-6.1], [3.9,0.4,2.1],[7.3,-9.9,-4.5]])

print(X)
```
