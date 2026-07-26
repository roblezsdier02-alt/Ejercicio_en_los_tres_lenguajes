# Trabajo en C

## Descripción
En esta carpeta se encuentra el programa desarrollado en lenguaje C para realizar operaciones con matrices 2x3.

## Código
```c
#include <stdio.h>
//Funciones utilizadas
void completarMatrices(int matrizA[2][3], int matrizB[2][3]);
void sumaMatriz(int matrizA[2][3], int matrizB[2][3], int resultado[2][3]);
void restaMatriz(int matrizA[2][3], int matrizB[2][3], int resultado[2][3]);
void multiplicacionMatriz(int matrizA[2][3], int matrizB[2][3], int resultado[2][3]);
void mostrarResultado(int resultado[2][3], char operacion[]);

int main(){
    // Declaración de las matrices
    int matrizA[2][3];
    int matrizB[2][3];

    // Matrices donde se almacenarán los resultados
    int suma[2][3];
    int resta[2][3];
    int multiplicacion[2][3];

    // Se ingresan los datos de las dos matrices
    completarMatrices(matrizA, matrizB);

    // Se realizan las operaciones
    sumaMatriz(matrizA, matrizB, suma);
    restaMatriz(matrizA, matrizB, resta);
    multiplicacionMatriz(matrizA, matrizB, multiplicacion);

    // Se muestran los resultados
    mostrarResultado(suma, "SUMA");
    mostrarResultado(resta, "RESTA");
    mostrarResultado(multiplicacion, "MULTIPLICACION");

    return 0;
}

/*
 Función: completarMatrices
 Objetivo: Solicitar al usuario los valores de las matrices.*/
void completarMatrices(int matrizA[2][3], int matrizB[2][3]){
    int i, j;

    printf("========== MATRIZ A ==========\n");

    for(i=0;i<2;i++){
        for(j=0;j<3;j++){
            printf("Ingrese A[%d][%d]: ",i,j);
            scanf("%d",&matrizA[i][j]);
        }
    }

    printf("\n========== MATRIZ B ==========\n");

    for(i=0;i<2;i++){
        for(j=0;j<3;j++){
            printf("Ingrese B[%d][%d]: ",i,j);
            scanf("%d",&matrizB[i][j]);
        }
    }
}

/*
 Función: sumaMatriz
 Objetivo: Sumar las dos matrices posición por posición.*/
void sumaMatriz(int matrizA[2][3], int matrizB[2][3], int resultado[2][3]){
    int i,j;

    for(i=0;i<2;i++){
        for(j=0;j<3;j++)
        {
            resultado[i][j]=matrizA[i][j]+matrizB[i][j];
        }
    }
}

/*
 Función: restaMatriz
 Objetivo: Restar las dos matrices posición por posición.*/
void restaMatriz(int matrizA[2][3], int matrizB[2][3], int resultado[2][3]){
    int i,j;

    for(i=0;i<2;i++){
        for(j=0;j<3;j++){
            resultado[i][j]=matrizA[i][j]-matrizB[i][j];
        }
    }
}

/*
 Función: multiplicacionMatriz
 Objetivo:Va a Multiplicar cada elemento de una matriz con la misma posición de la otra matriz.*/
void multiplicacionMatriz(int matrizA[2][3], int matrizB[2][3], int resultado[2][3]){
    int i,j;

    for(i=0;i<2;i++) {
        for(j=0;j<3;j++){
            resultado[i][j]=matrizA[i][j]*matrizB[i][j];
        }
    }
}

//Función: mostrarResultado
//Esta funcioón va a mostrar cualquier matriz resultado.
void mostrarResultado(int resultado[2][3], char operacion[]){
    int i,j;

    printf("\n==== %s ====\n",operacion);

    for(i=0;i<2;i++){
        for(j=0;j<3;j++){
            printf("%4d",resultado[i][j]);
        }
        printf("\n");
    }
}
