
#include <stdio.h>
 #include <stdlib.h>

 int main()
 {
   tt:
   system("title gerador de senhas");
   printf("\t\t################################################");
   printf("\n\t\t## BEM VINDO AO GERADOR DE SENHAS ALEATORIAS! ##\n");
   printf("\t\t## Programadores: Alan Iwson, Rogerio.   ##\n");
   printf("\t\t################################################\n\n\n");

   int menu, quant, quant1, num,i;
   int soma1, soma2, sair, s, tu, eu;
   char letras[]={"qwerty9ui6op3as8df5gh2jk7lz4xc1vb0nm"};
   char letras2 []={"qwertyuiopasdfghjklzxcvbnm"};


   alpha:
   printf("-------------------------------");
   printf("\n|Escolha uma das opcoes abaixos:|\n");
   printf("|1- Senhas somente com letras   |\n");
   printf("|2-Senhas somente com numeros   |\n");
   printf("|3-Senhas com letras e numeros  |\n");
   printf("|4-Fechar programa              |\n");
   printf("*-------------------------------*\n");
   scanf("%i", &menu);
   system("cls");

   switch (menu)
   {
          case 1:
               printf("\t\t*-------------------------------*\n");
               printf("\t\t|Voce escolheu senhas com letras|\n");
               printf("\t\t*-------------------------------*\n\n");
               tts:
               printf("Digite a quantidade de senhas que deseja gerar:\n");
               scanf("%i", &tu);
               system("cls");
               printf("Digite o numero de caracteres desejados sendo o minino 4 e o maximo 16:\n");
               scanf("%i", &eu);
               if((eu<4)||(eu>16))goto tts;
              system("cls");

              printf("\n");
         for (quant=1; quant<=tu; quant++)
          {
              for (quant1=1; quant1<=eu; quant1++)
              {
                s=rand()%25;
                printf("%c",letras2[s]);
              }
             printf("\n");
         }

          break;

          case 2:
               printf("\t\t*----------------------------------*\n");
               printf("\t\t| Voce escolheu senhas com numeros |\n");
               printf("\t\t*----------------------------------*\n\n");
               ts:
               printf("Digite a quantidade de senhas que deseja gerar:\n");
               scanf("%i", &tu);
               system("cls");
               printf("Digite o numero de caracteres desejados sendo o minimo 4 e o maximo 16:\n");
               scanf("%i", &eu);
               system("cls");
               if((eu<4)||(eu>16))goto ts;

              printf("\n");

          for (quant=1; quant<=tu; quant++)
          {
              for (quant1=1; quant1<=eu; quant1++)
              {
                s=rand()%9;
                printf("%i",s);
              }
             printf("\n");
         }
          break;

          case 3:
               printf("\t\t*--------------------------------------------*\n");
               printf("\t\t| Voces escolheu senhas com numeros e letras |\n");
               printf("\t\t*--------------------------------------------*\n*");
               tr:
               printf("Digite a quantidade de senhas que deseja gerar:\n");
               scanf("%i", &tu);
               system("cls");
               printf("Digite o numero de caracteres desejados sendo o minino 4 e o maximo 16:\n");
               scanf("%i", &eu);
               if((eu<4)||(eu>16))goto tr;

               printf("\n");

         for (quant=1; quant<=tu; quant++)
          {
              for (quant1=1; quant1<=eu; quant1++)
              {
                s=rand()%35;
                printf("%c",letras[s]);
              }
             printf("\n");
         }
          break;

          case 4:
               printf("Tem certeza que deseja sair?\n");
               printf("1-Sim\n");
               printf("2-Nao\n");
               scanf("%i", &sair);

               if (sair==1)
               {
                exit (EXIT_SUCCESS);
               }
               else
               {
               system("cls");
               goto alpha;
               }
          break;

          default:
               printf("Comando invalido. Verifique as opcoes abaixo.\n\n");
               goto alpha;

          break;

   }
  system("pause");
  goto tt;
  return 0;
 }
