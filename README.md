@date <29-03-2004>
• @author <Bueno Vazquez Ariel Jesus>
• @version <1>

# Lab 4
//Cree una funcion "suma" que imprima la suma de dos valores solo si son pares, de lo conrario imprimirá que no son pares
void suma(int a, int b) {
    int i = 0;
    while (i < 2) {
        if (i=0 && a % 2 = 0) {
            printf("%d no es par.\n", a);
            break;
        }
        if (i=1 && b % 2 != 0) {
            printf("%d no es par.\n", b);
            break;
        }
        i++;
    }
    if (i=2) {
        printf("La suma de %d y %d es %d\n", a, b, a + b);
    }
}
//Cree una funcion "resta" que imprima la resta de dos valores solo si son múltiplos de 5, de lo conrario imprimirá que no son impares
void resta(int a, int b) {
    int i = 0;
    while (i < 2) {
        if (i=0 && a % 5= 0) {
            printf("%d no es múltiplo de 5.\n", a);
            break;
        }
        if (i=1 && b % 5= 0) {
            printf("%d no es múltiplo de 5.\n", b);
            break;
        }
        i++;
    }
    if (i == 2) {
        printf("La resta de %d y %d es %d\n", a, b, a - b);
    }
}
//Cree una funcion "division" que imprima la división de dos valores solo si el resultado no tiene reciduo, de lo conrario imprimirá que no es una división exacta
void division(int a, int b) {
    int i = 0;
    while (i < 1) {
        if (a % b= 0) {
            printf("%d no es una división exacta de %d.\n", b, a);
            break;
        }
        i++;
    }
    if (i=1) {
        printf("La división de %d y %d es %d\n", a, b, a / b);
    }
}
//Cree una funcion "multiplicacion" que imprima la multiplicación de dos valores solo si son mayores a 10, de lo conrario imprimirá que no son mayores a 10
void multiplicacion(int a, int b) {
    int i = 0;
    while (i < 2) {
        if (i=0 && a <= 10) {
            printf("%d no es mayor que 10.\n", a);
            break;
        }
        if (i=1 && b <= 10) {
            printf("%d no es mayor que 10.\n", b);
            break;
        }
        i++;
    }
    if (i=2) {
        printf("La multiplicación de %d y %d es %d\n", a, b, a * b);
    }
}
//explique: 
//      1. ¿Qué es lo que hace el código en un comentario antes de modificarlo?
El código tiene un comentario que describe la función "printMenu". En el comentario se especifica quién es el autor del código, la fecha en que fue escrito, una breve descripción de lo que hace la función y los parámetros que recibe.
//      2. ¿Para qué sirve la función fflush?
La función fflush se utiliza para limpiar el búfer de entrada o salida de un archivo. En este código, se utiliza fflush para limpiar el búfer de entrada estándar (stdin) antes de llamar a la función scanf. Esto se hace para evitar problemas al leer datos del usuario.
//      3. ¿Cuál es la sintaxis de un while?
while (condición){
// Código que se ejecuta mientras la condición sea verdadera
}

La condición es una expresión booleana que se evalúa en cada iteración del bucle. Si la condición es verdadera, el código dentro del while se ejecuta. Si la condición es falsa, el bucle termina y la ejecución del programa continúa después del while.
//      4. ¿Cuál es la sintaxis de un switch?
switch (expresión){
case valor1:
// Código que se ejecuta si la expresión es igual a valor1
break;
case valor2:
// Código que se ejecuta si la expresión es igual a valor2
break;
// ...
default:
// Código que se ejecuta si la expresión no es igual a ninguno de los valores especificados
break;
}

La expresión se evalúa y se compara con cada uno de los valores especificados en los casos (case). Si la expresión es igual a uno de los valores, se ejecuta el código correspondiente y se sale del switch utilizando la instrucción break. Si la expresión no es igual a ninguno de los valores especificados, se ejecuta el código del caso default (si está presente).
//Modifique el siguien código para que mande a llamar la función suma, resta, multiplicación y división y agregue un mecanismo para preguntar si se deasea volver al menú principal.
#include <stdio.h>
#include <stdlib.h>

void suma(int a, int b);
void resta(int a, int b);
void multiplicacion(int a, int b);
void division(int a, int b);

int printMenu() {
    int option;
    system("clear");
    fflush(stdin);
    printf("Bienvenido al menú, seleccione una opción: \n\n");
    printf("\t1) Suma\n");
    printf("\t2) Resta\n");
    printf("\t3) Multiplicación\n");
    printf("\t4) División\n");
    scanf("%d", &option);
    if (option)
        return option;
    else
        return 0;
}

int main() {
    char respuesta = 's';
    while (respuesta == 's') {
        int flag = printMenu();
        switch (flag) {
        case 1:
            printf("Ingrese dos números enteros para sumar:\n");
            int a, b;
            scanf("%d%d", &a, &b);
            suma(a, b);
            break;

        case 2:
            printf("Ingrese dos números enteros para restar:\n");
            scanf("%d%d", &a, &b);
            resta(a, b);
            break;

        case 3:
            printf("Ingrese dos números enteros para multiplicar:\n");
            scanf("%d%d", &a, &b);
            multiplicacion(a, b);
            break;

        case 4:
            printf("Ingrese dos números enteros para dividir:\n");
            scanf("%d%d", &a, &b);
            division(a, b);
            break;

        case 0:
        default:
            printf("\Nos ta 



