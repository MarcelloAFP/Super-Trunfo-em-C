#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include <time.h>

// Estrutura da carta
typedef struct {
    char nome[50];
    int poder;
    int velocidade;
} Carta;

// Função para criar o baralho
void criarBaralho(Carta baralho[], int tamanho) {
    strcpy(baralho[0].nome, "Carta A");
    baralho[0].poder = 10;
    baralho[0].velocidade = 5;

    strcpy(baralho[1].nome, "Carta B");
    baralho[1].poder = 7;
    baralho[1].velocidade = 8;

    strcpy(baralho[2].nome, "Carta C");
    baralho[2].poder = 9;
    baralho[2].velocidade = 6;

    strcpy(baralho[3].nome, "Carta D");
    baralho[3].poder = 5;
    baralho[3].velocidade = 10;

    strcpy(baralho[4].nome, "Carta E");
    baralho[4].poder = 11;
    baralho[4].velocidade = 4;
}

//Função para embaralhar o baralho
void embaralhar(Carta baralho[], int tamanho){
    srand(time(NULL));
    for (int i = tamanho - 1; i > 0; i--){
        int j = rand() % (i + 1);
        Carta temp = baralho[i];
        baralho[i] = baralho[j];
        baralho[j] = temp;
    }
}

int main() {
    Carta baralho[5];
    criarBaralho(baralho, 5);
    embaralhar(baralho, 5);

    Carta jogador = baralho[0];
    Carta computador = baralho[1];

    printf("Sua carta:\n");
    printf("Nome: %s\n", jogador.nome);
    printf("Poder: %d\n", jogador.poder);
    printf("Velocidade: %d\n", jogador.velocidade);

    printf("\nCarta do computador:\n");
    printf("Nome: %s\n", computador.nome);
    printf("Poder: %d\n", computador.poder);
    printf("Velocidade: %d\n", computador.velocidade);

    int escolha;
    printf("\nEscolha o atributo (1: Poder, 2: Velocidade): ");
    scanf("%d", &escolha);

    int resultado;
    if (escolha == 1) {
        resultado = jogador.poder - computador.poder;
    } else {
        resultado = jogador.velocidade - computador.velocidade;
    }

    if (resultado > 0) {
        printf("Você venceu!\n");
    } else if (resultado < 0) {
        printf("Você perdeu!\n");
    } else {
        printf("Empate!\n");
    }

    return 0;
}
