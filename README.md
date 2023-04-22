# Programación de Computadores - UNAL
# Matrices

Una matriz es un arreglo rectangular de elementos del mismo tipo, esto es una colección de *n* x *m* arreglos.

**Ejemplo 1:** Matriz de 2 filas y 3 columnas.

$$\begin{matrix}
1 & 2 & 3\\
4 & 5 & 6
\end{matrix}$$

En forma general una matriz se representa de la forma:

<div align='center'>
<figure> <img src="https://i.postimg.cc/Px3TQ3kz/image.png" alt="" width="600" height="auto"/></br>
<figcaption><b></b></figcaption></figure>
</div>

Para acceder a un componente se requiere la pareja de coordenadas (i, j) que representan su ubicación en términos de fila y columna.

<div align='center'>
<figure> <img src="https://i.postimg.cc/MZnvrRrK/image.png" alt="" width="600" height="auto"/></br>
<figcaption><b></b></figcaption></figure>
</div>

En **Python** una matríz de *n* x *m* es un arreglo de *n* arreglos (filas) com *m* elementos cada uno.

**Ejemplo 2:** Representar la matriz **A**: 

$$A \ = \ \begin{matrix}
1 & 2 & 3\\
4 & 5 & 6 \\
7 & 8 & 9
\end{matrix}$$

```python
fila1 = [1, 2, 3]
fila2 = [4, 5, 6]
fila3 = [7, 8, 9]
A = [fila1, fila2, fila3]
# A = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
print(A) 
```

**Ejemplo 3:** Acceder al elemento fila 2 columna 3 de **A**:
```python
A = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
print(A[1][2]) 
```

**Ejemplo 4:** Recorrer la matriz **A**:
```python
A = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
for i in range(len(A)): # Recorre filas
  for j in range(len(A[i])): # Recorre cada elemento de la fila
    print(A[i][j])
```

**Ejemplo 5:** Generar una matriz 3 x 3 con los cuadrados del 1 al 9:
```python
B = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
for i in range(len(B)): # Recorre filas
  for j in range(len(B[i])): # Recorre cada elemento de la fila
    B[i][j] *= B[i][j]
print(B) 
```

```python
# Sin tener la matriz base
fils = []
B = []
num :  int = 1
for i in range(3): # Recorre filas
  for j in range(3): # Recorre cada elemento de la fila
    fils.append(num**2)
    num += 1
  B.append(fils)
  fils = []  
print(B) 
```
**Ejemplo 6:** Imprimir de la matriz de cuadrados en la forma que se debe ver una matriz.

```python
C = [[1, 4, 9], [16, 25, 36], [49, 64, 81]]
for i in range(len(C)):
  print(C[i])
```

**Ejemplo 7:** Dados el número de columnas y filas, generar una matriz de solo unos.

```python
def imprimirMatriz(mat):
  for i in range(len(mat)): print(mat[i])

if __name__ == "__main__":
  nFilas = int(input("Ingrese filas: "))
  nCols = int(input("Ingrese columnas: "))
  ones = []
  for i in range(nFilas):
    ones.append([1]*nCols)
  imprimirMatriz(ones)
```

**Ejemplo 8:** Dado el rango generar una [matriz identidad](https://es.wikipedia.org/wiki/Matriz_identidad) (matriz cuadrada con diagonal en unos).

```python
def imprimirMatriz(mat):
  for i in range(len(mat)): print(mat[i])

if __name__ == "__main__":
  rango = int(input("Ingrese rango: "))
  unit = []
  filas = []
  for i in range(rango):
    for j in range(rango):
      if i == j : filas.append(1)
      else: filas.append(0)
    unit.append(filas)
    filas = []
  imprimirMatriz(unit)
```

## Reto 11
Desarrolle la mayoría de ejercicios en clase, por cado punto resuelto en clase tendrá media décima en el examen 2 (creanme, las van a necesitar). Para cada punto cree un programa individual. Al finalizar suba todo a un repo y subalo al canal reto_11 en slack.

1. Desarrolle un programa que permita realizar la [suma/resta de matrices](https://es.wikipedia.org/wiki/Adici%C3%B3n_matricial). El programa debe validar las condiciones necesarias para ejecutar la operación.

2. Desarrolle un programa que permita realizar el [producto de matrices](https://es.wikipedia.org/wiki/Multiplicaci%C3%B3n_de_matrices). El programa debe validar las condiciones necesarias para ejecutar la operación.

3. Desarrolle un programa que permita obtener la  [matriz transpuesta](https://es.wikipedia.org/wiki/Matriz_transpuesta) de una matriz ingresada. El programa debe validar las condiciones necesarias para ejecutar la operación.

4. Desarrollar un programa que sume los elementos de una columna dada de una matriz.

5. Desarrollar un programa que sume los elementos de una fila dada de
una matriz.

**Nota:** Todos los puntos deben estar debidamente comentados y utilziar funciones para su desarrollo.

