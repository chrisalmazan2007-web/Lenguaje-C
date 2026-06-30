#include <stdio.h>
#include <math.h>

int main() {

    int opcion;
    float num1, num2, resultado;
    float cateto1, cateto2, hipotenusa;

    do {

        printf("\n===== MENU =====\n");
        printf("1. Division de dos numeros\n");
        printf("2. Raiz cuadrada\n");
        printf("3. Hipotenusa de un triangulo\n");
        printf("4. Salir\n");
        printf("Seleccione una opcion: ");
        scanf("%d", &opcion);

        switch(opcion){

            case 1:

                printf("Ingrese el primer numero: ");
                scanf("%f",&num1);

                printf("Ingrese el segundo numero: ");
                scanf("%f",&num2);

                if(num2 != 0){
                    resultado = num1 / num2;
                    printf("Resultado = %.2f\n",resultado);
                }else{
                    printf("No se puede dividir entre cero.\n");
                }

                break;

            case 2:

                printf("Ingrese un numero: ");
                scanf("%f",&num1);

                if(num1 >= 0){
                    resultado = sqrt(num1);
                    printf("La raiz cuadrada es %.2f\n",resultado);
                }else{
                    printf("No existe raiz cuadrada de numeros negativos.\n");
                }

                break;

            case 3:

                printf("Ingrese el primer cateto: ");
                scanf("%f",&cateto1);

                printf("Ingrese el segundo cateto: ");
                scanf("%f",&cateto2);

                hipotenusa = sqrt(cateto1*cateto1 + cateto2*cateto2);

                printf("La hipotenusa es %.2f\n",hipotenusa);

                break;

            case 4:

                printf("Programa finalizado.\n");
                break;

            default:

                printf("Opcion incorrecta.\n");

        }

    }while(opcion != 4);

    return 0;
}
