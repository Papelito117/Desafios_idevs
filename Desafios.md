# Welcome to GitHub Desktop!
##desafio 1 em C++
#include <stdio.h>
#include <string.h>
#include <ctype.h>   
#include <string>
#include <cstdlib>
#include <fstream>

char intervalo1[] = "AEIOULNRSTaeioulsrt";
char intervalo2[] = "dgDG";
char intervalo3[] = "bcmpBCMP";
char intervalo4[] = "FHVWYfhvwt";
char intervalo5[] = "kK";                  
char intervalo6[] = "jqJQ";
char intervalo7[] = "qzQZ" ;
int main(){

    char palavra[20];
    int i, pontuacao = 0;

    fgets(palavra, 20, stdin);
    system("ls");

    for(i=0; i<strlen(palavra)-1; i++){
        pontuacao += getPontuacao(palavra[i]);
    }

    printf("Palavra: %sPontuacao total: %d\n", palavra, pontuacao);

    return 0;
}

int getPontuacao(char *letra){

    if(intervalo(intervalo1, letra)){
        return 1;
    }
    else if(intervalo(intervalo2, letra)){
        return 2;
    }
    else if(intervalo(intervalo3, letra)){
        return 3;
    }
        else if(intervalo(intervalo4, letra)){
        return 4;
    }
    else if{(intervalo(intervalo5,letra))
     return 5;
	}
	else if(intervalo(intervalo6, letra)){
      return 6;
	}else if(intervalo(intervalo7(,letra)){
		return7;
	}
    else return 0;

}

int intervalo(char *intervalo, char *letra){
    int i;
    for(i=0; i<strlen(intervalo); i++){
        if(toupper(letra) == intervalo[i]){
            return 1;
        }
    }
    return 0;
}

### desafio 2 em C++

#include <string.h>
#include <ctype.h>
#include <string>
#include <cstdlib>
#include <fstream>

int main(void) {
	setlocale(LC_ALL, "portuguese");
    int numero, quantidadeDeDivisores;
    
    printf(" Insira um numero: ");
    scanf("%d", &numero);
    
    printf("\n D(%d): ", numero);
    
   
    for (int i = numero; i >= 1; --i) {
        
        if (numero % i == 0) {
            printf(" %d ", i);
            
        }
    } 
    
    system("pause");
    return 0;
    
}

### Desafio 3 em C++

#include <stdio.h>

main() {
	int a =1,b,f,i,r,min,max,z;
	printf("Digite valor :\n");
	scanf("%d",&b);
	    min=a; max=b;
    
i=2; z=0; f=0;

while(min<=max) {
    while(min>=i) {
        r=min%i;
    if (r==0)
        z=z+1; i=i+1;
    }
    if (z==1){
        f=f+1;  if (f==1)
                    printf("(%d",min);
            else if (f>1)
                    printf(", %d",min);
    }
    min=min+1; i=2; z=0;
    }
if (f>0)
    printf(")\n\n");
else
    printf("Sem valores nesse intervalo.\n\n");
getchar();
}