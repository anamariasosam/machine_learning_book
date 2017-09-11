### K-means

K grupo, cada k grupo tiene un centroide(el elememnto para separarlos, para definirme el patrón de cada grupo).
Luego toma la distancia de los datos al centroide, asignadole el grupo al que tenga la distancia mas cortica.

cuando el centroide se deje de mover para el algoritmos.
Cada que pasa una interación el centroide se reubica

K means +++: Ubicar los centroides más lejos posibles, para que converja más rápido

X: Variables latentes (están ocultas)


```python
import numpy as np
import matplotlib.pyplot as plt
from sklearn.cluster import KMeans
from sklearn import cluster

X = np.loadtxt("data_clustering.txt", delimiter = ',')
x_vals, y_vals = X[:,0], X[:,1]

# Visualizamos los datos para observar la disperción
plt.figure()
plt.scatter(x_vals, y_vals , marker = 'o', s=80, edgecolors='black', facecolors = 'none' ,linewidth=1)
x_min, x_max = x_vals.min() - 1 , x_vals.max() + 1
y_min, y_max = y_vals.min() - 1, y_vals.max() + 1
plt.title('Datos de entrada')
plt.xlim(x_min,x_max )
plt.ylim(y_min,y_max )
plt.xticks(())
plt.yticks(())
plt.show()


num_cluster = 5

modelo_kmeans = KMeans(init = 'k-means++', n_clusters = num_cluster, n_init = 10) # init establece el método de localización inicial de los centroides
modelo_kmeans.fit(X)
```

```python

# Visualizamos el resultado

paso = 0.01

# Puntos extremos de la malla
x_min, x_max = X[:,0].min() - 1 , X[:,0].max() + 1
y_min, y_max = X[:,1].min() - 1, X[:,1].max() + 1

# Asignamos los valores a la malla
x_vals, y_vals = np.meshgrid(np.arange(x_min, x_max, paso), np.arange(y_min, y_max, paso))

salida = modelo_kmeans.predict(np.c_[x_vals.ravel(), y_vals.ravel()])
salida = salida.reshape(x_vals.shape)

plt.figure()
plt.clf()
plt.imshow(salida, interpolation='nearest', extent = (x_vals.min(), x_vals.max(), y_vals.min(), y_vals.max()), cmap=plt.cm.Set2, aspect = 'auto', origin='lower')


plt.scatter(X[:,0], X[:,1], marker = 'o', facecolor='none', edgecolors='black', s=80)

centroides = modelo_kmeans.cluster_centers_

plt.scatter(centroides[:,0], centroides[:,1], marker='*', s = 210, linewidths= 4, facecolors = 'pink')

plt.title('Limites de los grupos')
plt.xlim(x_min,x_max )
plt.ylim(y_min,y_max )
plt.xticks(())
plt.yticks(())
plt.show()
```
