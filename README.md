# ExercicioEngenhariaSoftware
Programa que le o nome e a data nascimento e informa a idade atual de uma pessoa.
#include <stdio.h>
#include <time.h>
#include <stdlib.h>
#include <windows.h>
int main (){
    time_t mytime;
    mytime = time(NULL);
    struct tm tm = *localtime(&mytime);
    char name[20];
    int dia,mes,ano,diaAtual,mesAtual,anoAtual,idade=0;

    diaAtual=tm.tm_mday;
    mesAtual=tm.tm_mon + 1;
    anoAtual=tm.tm_year+1900;

    printf("Digite seu nome: ");
    scanf("%s",name);
    printf("\n\n");
    printf("%s digite o dia em que nasceu: ",name);
    scanf("%i",&dia);
    printf("\n\n");
    printf("Digite o mes em que nasceu: ");
    scanf("%i",&mes);
    printf("\n\n");
    printf("Digite o ano em que nasceu: ");
    scanf("%i",&ano);
    Sleep(1000);
    system("cls");
    if(mesAtual<=mes){
        if(diaAtual<dia)
                ano++;
    }
    printf("\n%s voce tem %i anos\n",name,idade=anoAtual-ano);
    return 0;
}
