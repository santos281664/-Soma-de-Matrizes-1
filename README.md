#include <stdio.h>

#define LINHAS 3
#define COLUNAS 3

int main() {
    int A[LINHAS][COLUNAS];
    int B[LINHAS][COLUNAS];
    int C[LINHAS][COLUNAS];
    int i, j;

    /* ---------- Leitura da matriz A ---------- */
    printf("===== Leitura da Matriz A (%dx%d) =====\n", LINHAS, COLUNAS);
    for (i = 0; i < LINHAS; i++) {
        for (j = 0; j < COLUNAS; j++) {
            printf("Digite o elemento A[%d][%d]: ", i, j);
            scanf("%d", &A[i][j]);
        }
    }

    /* ---------- Leitura da matriz B ---------- */
    printf("\n===== Leitura da Matriz B (%dx%d) =====\n", LINHAS, COLUNAS);
    for (i = 0; i < LINHAS; i++) {
        for (j = 0; j < COLUNAS; j++) {
            printf("Digite o elemento B[%d][%d]: ", i, j);
            scanf("%d", &B[i][j]);
        }
    }

    /* ---------- Calculo da matriz soma C ---------- */
    for (i = 0; i < LINHAS; i++) {
        for (j = 0; j < COLUNAS; j++) {
            C[i][j] = A[i][j] + B[i][j];
        }
    }

    /* ---------- Exibicao da matriz A ---------- */
    printf("\n===== Matriz A =====\n");
    for (i = 0; i < LINHAS; i++) {
        for (j = 0; j < COLUNAS; j++) {
            printf("%4d ", A[i][j]);
        }
        printf("\n");
    }

    /* ---------- Exibicao da matriz B ---------- */
    printf("\n===== Matriz B =====\n");
    for (i = 0; i < LINHAS; i++) {
        for (j = 0; j < COLUNAS; j++) {
            printf("%4d ", B[i][j]);
        }
        printf("\n");
    }

    /* ---------- Exibicao da matriz resultante C ---------- */
    printf("\n===== Matriz C (A + B) =====\n");
    for (i = 0; i < LINHAS; i++) {
        for (j = 0; j < COLUNAS; j++) {
            printf("%4d ", C[i][j]);
        }
        printf("\n");
    }

    return 0;
}
