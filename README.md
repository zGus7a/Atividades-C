Ativade 1 
#include <stdio.h>

int main () {
   int portuacoer
   int i; j;

for (i=o; i<3; i++) {
  for (j=0; j+5; j++) {
   printf("Digite a pontuação do joagdor  %d no jogo %d:" i+1; j+1);
  scanf("%d", &pontuações [i] [j]);
 }
}

 printf("Em matriz de pontuacoes: \n");
 for (i = o, i < 3; i++) {
 for (j= o; j<5; j++)
  printf("%d", pontuacoes [i] [j]);
 }
 printf("\n")
}
return 0;
}

Atividade 2

1- #include <stdio.h>
#include <stdbool.h>

bool primo(int num) {
    if (num < 2) {
        return false;
    }
    for (int i = 2; i * i <= num; i++) {
        if (num % i == 0) {
            return false;
        }
    }
    return true;
}

int somaPrimos(int N) {
    int soma = 0;
    int contagem = 0;
    int numero = 2; // Começamos a verificar a partir do primeiro primo

    while (contagem < N) {
        if (primo(numero)) {
            soma += numero;
            contagem++;
        }
        numero++;
    }

    return soma;
}

int main() {
    int N;

    printf("Digite o valor de N: ");
    scanf("%d", &N);

    int resultado = somaPrimos(N);
    printf("A soma dos %d primeiros números primos é: %d\n", N, resultado);

    return 0;
}

6 - #include <stdio.h>

int maiorNumero(int a, int b);

int main() {
    int num1, num2;

    printf("Digite o primeiro número: ");
    scanf("%d", &num1);
    printf("Digite o segundo número: ");
    scanf("%d", &num2);

    int maior = maiorNumero(num1, num2);
    printf("O maior número é: %d\n", maior);

    return 0;
}

int maiorNumero(int a, int b) {
    if (a > b) {
        return a;
    } else {
        return b;
    }
}


7 - #include <stdio.h>

int calcularSoma(int vetor[], int tamanho);

int main() {
    int numeros[3]; // Vetor para armazenar três números inteiros

    for (int i = 0; i < 3; i++) {
        printf("Digite o %dº número: ", i + 1);
        scanf("%d", &numeros[i]);
    }

    int soma = calcularSoma(numeros, 3);
    printf("A soma dos valores é: %d\n", soma);

    return 0;
}

int calcularSoma(int vetor[], int tamanho) {
    int soma = 0;
    for (int i = 0; i < tamanho; i++) {
        soma += vetor[i];
    }
    return soma;
}

5 - #include <stdio.h>

int somar(int a, int b);

int main() {
    int num1, num2;

    printf("Digite o primeiro número: ");
    scanf("%d", &num1);
    printf("Digite o segundo número: ");
    scanf("%d", &num2);

    int resultado = somar(num1, num2);
    printf("A soma de %d e %d é: %d\n", num1, num2, resultado);

    return 0;
}

int somar(int a, int b) {
    return a + b;
}

Atividade 3 

 #include <stdio.h> //Cria uma biblioteca//
 //Gustavo Montico
 typedef struct { //Cria uma estruturação com as informações brevemente solicitadas
 double peso;
 int idade;
 double altura;
 } pessoa;
 void imprimePessoa (pessoa p) {
 printf("Peso: %lf. Idade: %d. Altura: %lf. \n\n", p.peso, p.idade, p.altura); //Cria uma função
 que imprime uma estrutura pessoa contendo parametros como peso, idade e altura
 }
 int main() { //Declara um vetor com 5 elementos do tipo pessoa contendo uma variável p1 do
 tipo pessoa
 pessoa pessoas [5], p1;
 pessoas [0].peso = 80.6; // Inicializa o primeiro elemento do vetor pessoas com valores
 especificos para peso, idade e altura.
 pessoas [0].idade = 40;
 pessoas [0].altura = 1.70;
 p1 = pessoas [0]; //Atribui ao p1 os valores do primeiro elemento de pessoas.
 if (p1.idade > 20) //Verifica se a idade de p1 é maior que 20; se for, adiciona a idade em 1.
 p1.idade++;
 pessoas [1] = pessoas [0]; //Copia o conteúdo do primeiro elemento de pessoas para o
 segundo elemento do vetor.
 imprimePessoa (p1);
 imprimePessoa (pessoas [0]);
 imprimePessoa (pessoas [1]);
 imprimePessoa (pessoas [2]);
 imprimePessoa (pessoas [3]);
 imprimePessoa (pessoas [4]);
 return 0; //Fim do programa

—------------------------------------------

#include <stdio.h>
 //Gustavo Montico
 typedef struct {
 double peso;
 int idade;
 double altura;
 } pessoa;
void imprimePessoa(pessoa p) {
 printf("Peso: %.2lf. Idade: %d. Altura: %.2lf\n", p.peso, p.idade, p.altura);
 }
 void lePessoa(pessoa *p) {
 printf("Digite o peso: ");
 scanf("%lf", &p->peso);
 printf("Digite a idade: ");
 scanf("%d", &p->idade);
 printf("Digite a altura: ");
 scanf("%lf", &p->altura);
 }
 int main() {
 pessoa pessoas[5];
 // Lê os dados das 5 pessoas
 for (int i = 0; i < 5; i++) {
 printf("\nPessoa %d:\n", i + 1);
 lePessoa(&pessoas[i]);
 }
 // Imprime os dados das 5 pessoas
 for (int i = 0; i < 5; i++) {
 printf("\nDados da pessoa %d:\n", i + 1);
 imprimePessoa(pessoas[i]);
 }
 return 0;
 }


—------------------------------

2) 
//Gustavo Montico
#include // inclui a biblioteca padrão de entrada e saída, que permite o uso de funções como printf.
 #include // inclui a biblioteca para manipulação de strings, usada para copiar strings. #include // permite definir configurações regionais, como o uso de caracteres acentuados no 
console.
 typedef struct { // Define uma estrutura chamada Carro, que contém três campos. 
char modelo [50]; // uma string de 50 caracteres para armazenar o modelo do carro.
int ano// um inteiro para armazenar o ano de fabricação. double preco; // um número de ponto flutuante do tipo double para armazenar o preço do carro. } 
Carro; void modificarPreco (Carro *c, double novoPreco) { // Declara uma função modificarPreco, que altera o preço de um carro:
 c->preco = novoPreco; // Recebe um ponteiro para um objeto do tipo Carro e um valor novoPreco. } 
// Usa c->preco = novoPreco para alterar o preço do carro apontado. void imprimirCarro (Carro *c) { // Declara a função imprimirCarro, que exibe as informações de umcarro: 
printf("Modelo: %s\n", c->modelo); // Recebe um ponteiro para Carro e usa printf para mostrar o modelo, o ano e o preço, formatado com duas casas decimais.
 printf("Ano: %d\n", c->ano); printf("Preço: R$ %.21f\n", c->preco); } 
int main() { // Define a função main, que é o ponto de entrada do programa: 
setlocale (LC_ALL, "portuguese"); // setlocale(LC_ALL, "portuguese"); define a configuração regional para "portuguese", permitindo caracteres especiais.
 Carro carrol; // Declara uma variável carrol do tipo Carro. 
strcpy (carrol.modelo, "xyz"); // Inicializa os valores dos campos de carrol:
 carrol.ano=2020; // Define o ano como 2020 e o preco como 90000.00. carrol.preco = 90000.00; 
printf("Dados antes da modificação:\n"); // imprimirCarro(&carrol); chama a função imprimirCarro, passando o endereço de carrol. imprimirCarro (&carrol); 
modificar Preco (&carrol, 115000.00); // Chama a função modificarPreco para alterar o preço de carrol para 115000.00. 
printf("\nDados após a modificação do preço:\n"); //Exibe os dados do carro após a modificação, chamando novamente imprimirCarro.
 imprimirCarro (&carrol); 

return 0;  

}


—---------------------------------------------------
3) 
 //Gustavo Montico
 #include // Inclui a biblioteca padrão de entrada e saída em C (stdio.h), necessária para usar funções como printf. 
int calcularResultado (int v[], int n); //Declara a função calcularResultado, que será definida mais tarde no código. Ela recebe um vetor de inteiros v e um inteiro n, que representa o tamanho do vetor.
int main() {

 int vetor[5], i, resultado; //Declara vetor[5] como um array de 5 inteiros, i como uma variável de controle e resultado para armazenar o valor retornado pela função calcularResultado.

 for (i=0; i < 5; i++) { //A cada iteração, o elemento vetor[i] é preenchido com i * 2. Assim, o vetor conterá os valores: {0, 2, 4, 6, 8}. 

vetor[i]= i*2; } resultado = calcularResultado (vetor, 5); //Chama a função calcularResultado, passando o vetor vetor e o tamanho 5. Armazena o valor retornado na variável resultado.

printf("O resultado é: %d\n", resultado);//Exibe o valor de resultado no console. return 0; }

int calcularResultado (int v[], int n) { //Recebe um vetor v e um inteiro n, que representa o número de elementos no vetor
//Declara soma, inicializado em 0, para acumular a soma dos elementos.
 int i, soma = 0;
 for (i = 0; i < n; i++) { //A cada iteração, adiciona o valor v[i] à variável soma. soma += v[i]; } 

return soma; }




—----------------------------------

4) 
//Gustavo Montico
 #include <stdio.h>
 float calcularMedia(float n1, float n2, float n3, float n4) {
 return (n1 + n2 + n3 + n4) / 4;
 }
 
 int main() {
 
 float nota1, nota2, nota3, nota4;
 
 printf("Digite a primeira nota: ");
 scanf("%f", &nota1);
 printf("Digite a segunda nota: ");
 scanf("%f", &nota2);
 printf("Digite a terceira nota: ");
 scanf("%f", &nota3);
 printf("Digite a quarta nota: ");
 scanf("%f", &nota4);
 
 float media = calcularMedia(nota1, nota2, nota3, nota4);
 printf("Media: %.2f\n", media);
 if (media >= 7.0) {
 printf("Aprovado\n");
 } else {
 printf("Reprovado\n");
 }
 return 0;
 }


—-----------------

5) 
//Gustavo Montico
 #include <stdio.h>
 
 void exibirImparesExcetoMultiplosDe7(int numero) {
 printf("Numeros impares de 1 ate %d, exceto multiplos de 7:\n", numero);
 
 for (int i = 1; i <= numero; i++) {
 if (i % 2 != 0 && i % 7 != 0) {
 
 printf("%d ", i);
 }
 }
 
 printf("\n");
 }
 
 int main() {
 int numero;
 
 printf("Digite um numero: ");
 scanf("%d", &numero);
 
 exibirImparesExcetoMultiplosDe7(numero);
 
 return 0;
 }

—---------------------------

6) 
//Gustavo Montico
 #include <stdio.h>
 int somarValores(int vetor[], int tamanho) {
 int soma = 0;
 for (int i = 0; i < tamanho; i++) {
 soma += vetor[i];
 }
 return soma;
 }
 
 int main() {
 int tamanho;
 printf("Digite o tamanho do vetor: ");
 scanf("%d", &tamanho);
 
 int vetor[tamanho];
 printf("Digite os %d valores do vetor:\n", tamanho);
 
 for (int i = 0; i < tamanho; i++) {
 
 printf("Valor %d: ", i + 1);
 scanf("%d", &vetor[i]);
 }
 
 int soma = somarValores(vetor, tamanho);// Calcula a média
 
 float media = (float)soma / tamanho;
 printf("Soma dos valores: %d\n", soma);
 printf("Média dos valores: %.2f\n", media);
 
 return 0;
 
 }

—----------------------------
7) 
//Gustavo Montico
 #include <stdio.h>
 
 void ImprimaMaior(int *vetor, int tamanho) {
 
 int maior = *vetor;
 int posicao = 0;
 
 for (int i = 1; i < tamanho; i++) {
 
 if (*(vetor + i) > maior) {
 maior = *(vetor + i);
 posicao = i;
 }
 }
 
 printf("O maior número é: %d\n", maior);
 printf("A posição do maior número é: %d\n", posicao);
 }
 
 int main() {
 int n1, n2;
 int vetor[2];
 
 printf("Digite o primeiro número: ");
 scanf("%d", &n1);
 
 printf("Digite o segundo número: ");
 scanf("%d", &n2);
 
 vetor[0] = n1;
 vetor[1] = n2;
 
 ImprimaMaior(vetor, 2);
 
 return 0;
 }

—-------------------------------
8) 
//Gustavo Montico 
 #include <stdio.h>
 void exibirPares(int numero) {

 printf("Números pares de 1 até %d: ", numero);

 for (int i = 2; i <= numero; i += 2) {
 printf("%d", i);

 if (i < numero) {
 printf(", ");
 }
 }

 printf("\n");
 }

 int main() {
 int numero;

printf("Digite um número inteiro: ");
scanf("%d", &numero);

exibirPares(numero);

return 0;
 }

—-------------------

9)
//Gustavo Montico
 #include <stdio.h>
 int multiplicaVetor(int vetor[], int tamanho) {
 int resultado = 1;
 
 for (int i = 0; i < tamanho; i++) {
 resultado *= vetor[i];
 }
 
 return resultado;
 }
 
 int main() {
 int tamanho;
 
 printf("Digite o tamanho do vetor: ");
 scanf("%d", &tamanho);
 
 int vetor[tamanho];
 for (int i = 0; i < tamanho; i++) {
 
 printf("Digite o valor para a posicao %d: ", i + 1);
 scanf("%d", &vetor[i]);
 }
 
 int resultado = multiplicaVetor(vetor, tamanho);
 printf("O resultado da multiplicacao dos elementos do vetor e: %d\n", resultado);
 
 return 0;
 }

—-----------------------
10) 
//Gustavo Montico 
 #include <stdio.h>
 
 void maiorNumero(int num1, int num2) {
 
 if (num1 > num2) {
 printf("O maior numero e: %d\n", num1);
 } else if (num2 > num1) {
 printf("O maior numero e: %d\n", num2);
 } else {
 printf("Os numeros sao iguais: %d e %d\n", num1, num2);
 }
 }
 
 int main() {
 int num1, num2;
 
 printf("Digite o primeiro numero: ");
 scanf("%d", &num1);
 
 printf("Digite o segundo numero: ");
 scanf("%d", &num2);
 
 maiorNumero(num1, num2);
 
 return 0;
 }

—----------------------------
11) 
//Gustavo Montico
 #include <stdio.h>
 
 int menorNumero(int num1, int num2, int num3) {
 int menor = num1;
 
 if (num2 < menor) {
 menor = num2;
 }
 
 if (num3 < menor) {
 menor = num3;
 }
 
 return menor;
}
 
 int main() {
 int num1, num2, num3;
 
 printf("Digite o primeiro numero: ");
 scanf("%d", &num1);
 
 printf("Digite o segundo numero: ");
 scanf("%d", &num2);
 
 printf("Digite o terceiro numero: ");
 scanf("%d", &num3);
 
 int menor = menorNumero(num1, num2, num3);
 printf("O menor numero e: %d\n", menor);
 
 return 0;
 }

—------------------

12)
//Gustavo Montico
 #include <stdio.h>
 
 void exibirOrdemInversa(int vetor[], int tamanho) {
 
 printf("Numeros em ordem inversa:\n");

 for (int i = tamanho- 1; i >= 0; i--) {
 printf("%d ", vetor[i]);
 }

 printf("\n");
 }

 int main() {
 int vetor[10];

 for (int i = 0; i < 10; i++) {

 printf("Digite o numero %d: ", i + 1);
 scanf("%d", &vetor[i]);
 }

 exibirOrdemInversa(vetor, 10);

return 0;
 }

—-----------------

13)
//Gustavo Montico
 #include <stdio.h>
 
 float calcularMedia(int num1, int num2, int num3) {
 
 return (num1 + num2 + num3) / 3.0;
 }
 
 int main() {
 int num1, num2, num3;
 
 printf("Digite o primeiro numero: ");
 scanf("%d", &num1);
 
 printf("Digite o segundo numero: ");
 scanf("%d", &num2);
 
 printf("Digite o terceiro numero: ");
 scanf("%d", &num3);
 
 float media = calcularMedia(num1, num2, num3);
 printf("A media dos tres numeros e: %.2f\n", media);
 
 return 0;
 }

—---------------
14)
//Gustavo Montico
 #include <stdio.h>
 
 int calcularResultado(int soma, int primeiroValor, int ultimoValor) {
 int resultado = soma + (primeiroValor * 5) + (ultimoValor * 2);
 
 return resultado;
 }
 
 int main() {
 int vetor[10];
 int soma = 0;
 
 for (int i = 0; i < 10; i++) {
 vetor[i] = i + 1;
 soma += vetor[i];
 }
 
 int resultado = calcularResultado(soma, vetor[0], vetor[9]);
 
 printf("Resultado: %d\n", resultado);
 
 return 0;
 }


