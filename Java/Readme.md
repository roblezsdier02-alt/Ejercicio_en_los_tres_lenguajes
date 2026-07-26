# Trabajo en Java

## Descripción
En esta carpeta se encuentra el programa desarrollado en lenguaje java para realizar operaciones con matrices 2x3.

## Código
```java
import java.util.Scanner;

public class hola {

    // Método principal
    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);

        // Declaración de las matrices de 2 filas y 3 columnas
        int[][] matrizA = new int[2][3];
        int[][] matrizB = new int[2][3];

        // Matrices para guardar los resultados
        int[][] suma = new int[2][3];
        int[][] resta = new int[2][3];
        int[][] multiplicacion = new int[2][3];

        // Llamada al método que llena las matrices
        completarMatrices(matrizA, matrizB, entrada);

        // Operaciones posición por posición
        sumaMatriz(matrizA, matrizB, suma);
        restaMatriz(matrizA, matrizB, resta);
        multiplicacionMatriz(matrizA, matrizB, multiplicacion);

        // Mostrar resultados
        mostrarResultado(suma, "SUMA");
        mostrarResultado(resta, "RESTA");
        mostrarResultado(multiplicacion, "MULTIPLICACION");

        entrada.close();
    }

    // Función para ingresar los datos de las dos matrices
    public static void completarMatrices(int[][] matrizA, int[][] matrizB, Scanner entrada) {
        System.out.println("=========== MATRIZ A ===========");

        for (int i = 0; i < 2; i++) {
            for (int j = 0; j < 3; j++) {
                System.out.print("Ingrese A[" + i + "][" + j + "]: ");
                matrizA[i][j] = entrada.nextInt();
            }
        }

        System.out.println("\n=========== MATRIZ B ===========");

        for (int i = 0; i < 2; i++) {
            for (int j = 0; j < 3; j++) {
                System.out.print("Ingrese B[" + i + "][" + j + "]: ");
                matrizB[i][j] = entrada.nextInt();
            }
        }
    }

    // Función para sumar posición por posición
    public static void sumaMatriz(int[][] matrizA, int[][] matrizB, int[][] resultado) {
        for (int i = 0; i < 2; i++) {
            for (int j = 0; j < 3; j++) {
                resultado[i][j] = matrizA[i][j] + matrizB[i][j];
            }
        }
    }

    // Función para restar posición por posición
    public static void restaMatriz(int[][] matrizA, int[][] matrizB, int[][] resultado) {
        for (int i = 0; i < 2; i++) {
            for (int j = 0; j < 3; j++) {
                resultado[i][j] = matrizA[i][j] - matrizB[i][j];
            }
        }
    }

    // Función para multiplicar posición por posición
    public static void multiplicacionMatriz(int[][] matrizA, int[][] matrizB, int[][] resultado) {
        for (int i = 0; i < 2; i++) {
            for (int j = 0; j < 3; j++) {
                resultado[i][j] = matrizA[i][j] * matrizB[i][j];
            }
        }
    }

    // Función para mostrar una matriz resultado
    public static void mostrarResultado(int[][] resultado, String operacion) {
        System.out.println("\n=========== " + operacion + " ===========");

        for (int i = 0; i < 2; i++) {
            for (int j = 0; j < 3; j++) {
                System.out.printf("%6d", resultado[i][j]);
            }
            System.out.println();
        }
    }
}
```
## Captura de ejecución
<img width="407" height="637" alt="Captura de pantalla 2026-07-26 100249" src="https://github.com/user-attachments/assets/6725819b-afb9-48b5-9f2d-04ce23123e1a" />

[⬅️ Volver al README principal](../README.md)
