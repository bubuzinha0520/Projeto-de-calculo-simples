# Projeto-de-calculo-simples
//Pequeno sistema para um posto de combustível

#include<stdio.h>
#include<locale.h>
 
int main(){
	
	setlocale(LC_ALL,"Portuguese");
	
	float litros, valor;
	int tipo;
	
	printf("Tipo do combustível\n");
	printf("1 -  Àlcool\n");
	printf("2 - Gasolina\n");
	scanf("%d", &tipo);
	switch(tipo){
		
	case 1:
		printf("Valor em litros do combustível\n");
		scanf("%f", &litros);
		if(litros>25){
			valor= 3*litros;
			valor=valor -0.07*valor;
			printf("Valor a ser pago %.2f\n", valor);
		}else{
			valor=3*litros;
			valor=valor-0.09*valor;
			printf("Valor a ser pago %.2f\n", valor);
			
		}break;
		
	case 2:
		printf("Valor em litros do combustível\n", valor);
		scanf("%f", &litros);
	    if(litros<25){
	    	valor= 2*litros;
	    	valor= valor -0.05*valor;
	    	printf("Valor a ser pago %.2f\n", valor);
		}else{
			valor=2*litros;
			valor=valor -0.07*valor;
			printf("Valor a se pago %.2f\n", valor);
			
		}break;
		default:
			printf("Tipo de combustível ínvalido");
			
		return 0;	
		
	}
	   
	
