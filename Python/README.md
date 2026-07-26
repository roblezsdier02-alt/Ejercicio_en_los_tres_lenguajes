# Trabajo en Python

## Descripción
En esta carpeta se encuentra el programa desarrollado en lenguaje Python para realizar operaciones con matrices 2x3.

## Código
```python
# Programa para realizar suma, resta y multiplicación
# de dos matrices de 2 filas por 3 columnas

def main():
    matrizA = [[0 for j in range(3)] for i in range(2)]
    matrizB = [[0 for j in range(3)] for i in range(2)]

    suma = [[0 for j in range(3)] for i in range(2)]
    resta = [[0 for j in range(3)] for i in range(2)]
    multiplicacion = [[0 for j in range(3)] for i in range(2)]

    completarMatrices(matrizA, matrizB)

    sumaMatriz(matrizA, matrizB, suma)
    restaMatriz(matrizA, matrizB, resta)
    multiplicacionMatriz(matrizA, matrizB, multiplicacion)

    mostrarResultado(suma, "SUMA")
    mostrarResultado(resta, "RESTA")
    mostrarResultado(multiplicacion, "MULTIPLICACION")


def completarMatrices(matrizA, matrizB):
    print("=========== MATRIZ A ===========")


    for i in range(2):
        for j in range(3):
            matrizA[i][j] = int(input(f"Ingrese A[{i}][{j}]: "))

    print("\n=========== MATRIZ B ===========")


    for i in range(2):
        for j in range(3):
            matrizB[i][j] = int(input(f"Ingrese B[{i}][{j}]: "))


def sumaMatriz(matrizA, matrizB, resultado):
    for i in range(2):
        for j in range(3):
            resultado[i][j] = matrizA[i][j] + matrizB[i][j]


def restaMatriz(matrizA, matrizB, resultado):
    for i in range(2):
        for j in range(3):
            resultado[i][j] = matrizA[i][j] - matrizB[i][j]


def multiplicacionMatriz(matrizA, matrizB, resultado):
    for i in range(2):
        for j in range(3):
            resultado[i][j] = matrizA[i][j] * matrizB[i][j]


def mostrarResultado(resultado, operacion):
    print(f"\n=========== {operacion} ===========")

    for i in range(2):
        for j in range(3):
            print(f"{resultado[i][j]:6}", end="")
        print()


main()
```
## Captura de ejecución
<img width="422" height="627" alt="Captura de pantalla 2026-07-26 102518" src="https://github.com/user-attachments/assets/5f41cc62-a2ba-4a43-8cca-5979d78718f1" />

[⬅️ Volver al README principal](../README.md)
