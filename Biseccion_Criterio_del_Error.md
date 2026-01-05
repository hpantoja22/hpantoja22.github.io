# Resolución de Ecuaciones No Lineales

## Método de Bisección y Criterios de Error

### Autor

**Dr. Hermes Yesser Pantoja Carhuavilca**

---

## 📋 Enunciado

En muchos problemas de ingeniería es necesario resolver **ecuaciones no lineales** de la forma:

$$f(x) = 0$$

donde no existe una solución analítica cerrada, por lo que se recurre a **métodos numéricos iterativos**.  Uno de los métodos más robustos y conceptualmente simples es el **método de la bisección**. 

Consideremos la siguiente ecuación no lineal:

$$f(x) = x^3 - 4x - 9$$

Se sabe que esta ecuación tiene al menos una raíz real en el intervalo $[2, 3]$. 

---

## 📊 Datos

- **Función:**
  
  $$f(x) = x^3 - 4x - 9$$

- **Intervalo inicial:**
  
  $$[a, b] = [2, 3]$$

- **Precisión requerida:** 8 cifras significativas

---

## 🎯 Objetivos

1. Determinar el **número mínimo de iteraciones** necesarias para aproximar la raíz real de la ecuación usando el **método de la bisección** con **8 cifras significativas**.

2. Implementar el método de la bisección en **MATLAB**.

3. Analizar la **evolución del error relativo** en cada iteración. 

4. Visualizar gráficamente:
   - La función $f(x)$
   - La convergencia de la aproximación de la raíz

5. Utilizar un **control interactivo (slider)** para observar cómo el número de iteraciones afecta la precisión de la solución.

---

## 📖 Conceptos Teóricos

### Ecuaciones No Lineales

Una ecuación no lineal es aquella en la que la función $f(x)$ no es lineal. En general, este tipo de ecuaciones no puede resolverse de forma exacta, por lo que se emplean métodos numéricos iterativos.

---

### Método de la Bisección

El método de la bisección parte de un intervalo $[a, b]$ tal que: 

$$f(a) \cdot f(b) < 0$$

Esto garantiza, por el **Teorema del Valor Intermedio**, que existe al menos una raíz en el intervalo. 

En cada iteración se calcula el punto medio:

$$c = \frac{a + b}{2}$$

y se evalúa el signo de $f(c)$ para decidir el nuevo subintervalo que contiene la raíz: 

- Si $f(a) \cdot f(c) < 0$, entonces la raíz está en $[a, c]$
- Si $f(c) \cdot f(b) < 0$, entonces la raíz está en $[c, b]$

Este método garantiza convergencia, aunque puede ser lento comparado con otros métodos como Newton-Raphson o la Secante.

---

### Error Relativo y Cifras Significativas

El **error relativo aproximado** se define como: 

$$\delta_r = \left| \frac{x_k - x_{k-1}}{x_k} \right|$$

donde: 
- $x_k$ es la aproximación en la iteración $k$
- $x_{k-1}$ es la aproximación en la iteración anterior

Una aproximación tiene **$n$ cifras significativas** si cumple:

$$\delta_r \leq 5 \times 10^{-n}$$

Por ejemplo, para obtener **8 cifras significativas**, se requiere:

$$\delta_r \leq 5 \times 10^{-8}$$

---

## ❓ Preguntas

### 1. Número de Iteraciones

¿Cuántas iteraciones del método de la bisección son necesarias para aproximar la raíz de

$$x^3 - 4x - 9 = 0$$

con **8 cifras significativas**?

### 2. Implementación en MATLAB

Desarrolle un **Live Script en MATLAB** que:

- Implemente el **método de la bisección**.
- Calcule la aproximación de la raíz en cada iteración.
- Calcule y muestre el **error relativo**.
- Incluya un **slider interactivo** para variar el número de iteraciones. 
- Muestre:
  - El valor aproximado de la raíz.
  - El error relativo asociado.
  - La gráfica de la función $f(x)$ con la raíz aproximada.

### 3. Análisis de Resultados

Analice y comente:

- La velocidad de convergencia del método.
- La relación entre número de iteraciones y cifras significativas obtenidas. 
- Ventajas y limitaciones del método de bisección.

---

## 📚 Referencias

- Chapra, S. C., & Canale, R. P. (2015). *Métodos Numéricos para Ingenieros* (7ª ed.). McGraw-Hill.
- Burden, R. L., & Faires, J. D. (2010). *Numerical Analysis* (9th ed.). Brooks/Cole. 

---

*© 2026 - Material Didáctico de Métodos Numéricos*