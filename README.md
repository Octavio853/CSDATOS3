\# 📊 Clases y Métodos

\# Estructura de las clases:

\### `Estimacion`

Clase base para construir histogramas y estimar densidades con núcleos.

\*\*Métodos:\*\*

- `crear\_histograma(ancho\_banda)`
- `evaluar\_histograma(puntos\_x, ancho\_banda)`
- `estimar\_densidad(puntos\_eval, ancho\_banda, tipo\_nucleo)`

\*\*Núcleos:\*\*

- Gaussiano
- Rectangular
- Epanechnikov
- Triangular

\---

\### `AnalisisDescriptivo`

Es herencia de `Estimacion`. Te permite análisis estadísticos:

\*\*Funciones:\*\*

- Promedio, mediana, desviación, varianza.
- Cuartiles, mínimo, máximo.
- Gráfico Q-Q.
- Histogramas y densidades con núcleo.

\---

\### `GeneradorDeDatos`

Esta clase genera muestras aleatorias a partir de diversas distribuciones.

\*\*Métodos:\*\*

- `generar\_normal(media, desviacion)`
- `generar\_uniforme(inicio, fin)`
- `generar\_t(grados\_libertad, loc, escala)`
- `generar\_datos\_BS()`

Además incluye funciones de densidad teórica para cada distribución.

\---

\### `Regresion`

La clase que usamos para estimar modelos de regresión.

\*\*Funciones clave:\*\*

- `estimar\_modelo(X, Y)`
- `realizar\_prediccion(nuevos\_valores\_X)`

\---

\### `RegresionLineal`

Modelo de regresión lineal simple o múltiple. Como en el caso de AnalisisDescriptivo, tambien usamos herencia.

\*\*Funciones claves:\*\*

- `graficar\_ajuste()`
- `calcular\_coef\_correlacion()`
- `analizar\_errores()`
- `mostrar\_resultados()`
- `calcular\_intervalos()`

\---

\###`RegresionLinealSimple`

En este caso la llamamos subclase para los modelos lineales que tienen una sola variable predictora.

\---

\### 🧾 `RegresionLinealMultiple`

Al igual que en regresión lineal simple, pero la usamos en los modelos con múltiples variables predictoras.

\---

\### 🚦 `RegresionLogistica`

Esta clase permite modelar la relación entre una variable dependiente dummy (0 o 1) y un conjunto de variables independientes.

\*\*Funciones claves:\*\*

- `prediccion\_logistica(X, punto\_corte)`
- `evaluar\_modelo\_logistico(X, y)`
- `calcular\_bondad(X, y, umbral)`
- `puntos\_corte(X, y)`
- `graficar\_curva\_roc(X, y)`

\---

