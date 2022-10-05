#include <stdio.h>

int main(void) {
  int op;
  int num1;
  int num2;
  do{
  printf("Feita por :André Luiz Simão Alves\nCurso:Analise e desenvolvimento de sistema\nUniversidade La Salle\nMatricula:202211982\n");
  printf("Bem vindo a calculadora\n");
  printf("1 = Subtrair\n2 = Somar\n3 = Multiplicar\n4 = Dividir\n5 = Raiz quadrada\n6 = Potenciacao\n0 = Sair\nDigite um numero de acordo com oque deseja:");
  scanf("%d", &op);
  if(op > 0 && op <7){
  printf("Digite um valor:");
  scanf("%d",&num1);
  printf("Digite outro valor que deseja (somar, subtrair,Potenciar,\nMultiplicar , etc)\nCaso queira Fazer raiz quadrada digite 0:  ");
  scanf("%d",&num2);
    }
  switch(op){
    case 0:
      printf("SAINDO...\N");
    break;
    case 1:
      printf("Subtracao: %d\n", num1 - num2);
    break;
    case 2:
      printf("Soma: %d\n", num1 + num2);
    break;
    case 3:
    while(num2 == 0){
      printf("Nao existe divisao por zero\nDigite outro valor: ");
      scanf("%d", &num2);
    }
      printf("Multiplicação: %d\n", num1 * num2);
    break;
    case 4:
       printf("Divisao: %d\n", num1 / num2);
    break;
    case 5:
    while(num2 > 0){
      printf("Por favor Digite 0: ");
      scanf("%d", &num2);
    }
     printf("Sua raiz quadrada é; %.2f\n", sqrt(num1));
    break;
   case 6:
      printf("Seu valor é: %.0f\n", pow(num1, num2));
    break;
    default:
    printf("Opcao invalida.\nDigite outra opcao:  ");
  }
    }while (op != 0); 
}
