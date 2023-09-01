## Tarea 2: Triángulos
El siguiente documento contiene un algoritmo creado en 3 lenguajes de programación:

- Pseint (Pseudocódigo)
- C++
- Python
##
## Pseint

El siguiente programa creado en Pseint puede formar triángulos en 4 distintas posiciones. Triangulo que se muestre de arriba a derecha, de arriba a izquierda, de abajo a derecha y de abajo a izquierda. 

Se le agrego una funcionalidad en la cual el usuario puede escoger ya sea asteriscos u otro símbolo de preferencia, cualquiera de ellos va a crear los triángulos. 

Primero definimos la variables en este caso: cantidad, i, n, j como entero. Le solicitamos al usuario que ingrese la cantidad deseada y la guardamos en la variable "n", luego le solicitamos al usuario que nos indique el símbolo de preferencia a usar para formar el triangulo. Este dato se guarda en la variable "símbolo", luego se mostrara en pantalla una lista de opciones del 1 al 4 para imprimir la posición del triangulo deseado. Al momento de ingresar una de las opciones este numero será guardado en la variable "opcionMenu" 

Se utilizo  una estructura de control: "según" en la cual dependiendo de la opción que el usuario seleccione se ejecutara el caso correspondiente. Dentro de cada caso se utilizo un ciclo "for" para generar el patrón del triangulo deseado.  

**Caso 1: **
Este caso se utilizo dos bucles anidados. El primer bucle (`Para i <- 1 Hasta n Con Paso 1`) controla el número de filas en el triángulo (n) y el segundo bucle (`Para j <- 1 Hasta i Con Paso 1`) controla la cantidad de asteriscos en cada fila. En cada iteración del segundo bucle, se imprime el símbolo sin saltar línea, y después de cada fila se imprime una línea en blanco.

**Caso 2:**
Este caso también utiliza dos bucles anidados. El primer bucle (`Para i <- 0 Hasta n - 1 Con Paso 1`) controla el número de filas en el triángulo (n) y el segundo bucle (`Para j <- n - 1 Hasta i + 1 Con Paso -1`) imprime espacios en blanco antes de los asteriscos, seguido por otro bucle (`Para j <- 0 Hasta i Con Paso 1`) que imprime los asteriscos. Se imprime una línea en blanco después de cada fila.

**Caso 3:**
Este caso utiliza un bucle que va desde el número de filas inicial (n) hasta la cantidad especificada por el usuario. Un bucle interno controla la impresión de espacios en blanco antes de los asteriscos, y otro bucle imprime los asteriscos. Se imprime una línea en blanco después de cada fila.

**Caso 4:**
Este caso es similar al caso 3 pero invierte la dirección de los espacios en blanco. Comienza con la cantidad máxima de espacios en blanco y disminuye gradualmente hasta cero antes de imprimir los asteriscos. También se imprime una línea en blanco después de cada fila. 

*si el usuario coloca otro numero que no este dentro de las opciones, se agrego un "de otro modo" que le mostrara que la opción ingresada no es valida. Finalizando el programa*

cada caso se finaliza con un "fin para" y al final de los casos se finaliza con un Fin según y el final del algoritmo. 
En la parte de abajo encontrara el código fuente: 


        Algoritmo asteriscoTriangulo
    	Definir cantidad Como Entero;
    	Definir i, n, j Como Entero;
    	Escribir "Inserte la cantidad: ";
    	Leer n; 
    	Escribir "Indique el Simbolo";
    	Leer simbolo;
    	Escribir "Indique el Triángulo a imprimir";
    	Escribir "1. Arriba Derecha: ";
    	Escribir "2. Arriba Izquierda: ";
    	Escribir "3. Abajo Derecha: ";
    	Escribir "4. Abajo Izquierda: ";
    	Leer opcionMenu;
    	Segun opcionMenu Hacer
    		1: 
    			Para i <- 1 Hasta n Con Paso 1 
    				//aster
    				Para j <- 1 Hasta i Con Paso 1
    					Escribir simbolo Sin Saltar;
    				FinPara
    				Escribir "";
    			FinPara
    		2:
    			Para i <- 0 Hasta n - 1 Con Paso 1 Hacer
    				//aster
    				Para j <- n - 1 Hasta i + 1 Con Paso - 1 Hacer
    					Escribir Sin Saltar " ";
    				FinPara
    				Para j <- 0 Hasta i Con Paso 1 Hacer
    					Escribir simbolo Sin Saltar;
    				FinPara
    				Escribir " ";
    			FinPara
    		3:
    			Para i <- n Hasta cantidad Con Paso -1 Hacer
    				//espacios
    				Para j <- n Con Paso i - 1 Hasta i Hacer
    					Escribir Sin Saltar ""; 
    				FinPara
    				//aster
    				Para j <- 1 Con Paso 1 Hasta i Hacer
    					Escribir simbolo Sin Saltar;
    				FinPara
    				Escribir " ";
    			FinPara
    		4:
    			Para i <- n Hasta cantidad Con Paso - 1 Hacer
    				//espacios
    				Para j <- 0 Con Paso 1 Hasta (n -i -1) Hacer
    					Escribir " " Sin Saltar; 
    				FinPara
    				//aster
    				Para j <- 1 Con Paso 1 Hasta i Hacer
    					Escribir simbolo Sin Saltar;
    				FinPara
    				Escribir " ";
    			FinPara
    		De Otro Modo:
    			Escribir "Opcion no valida, por favor vuelva a intentarlo"
    	FinSegun
    FinAlgoritmo

## 
## C++

El siguiente programa creado en C++ puede formar triángulos en 4 distintas posiciones. Triangulo que se muestre de arriba a derecha, de arriba a izquierda, de abajo a derecha y de abajo a izquierda. 

Primero se incluye la librería  _"iostream"_  para manejar la entrada y salida estándar. Se utilizó la función  _"main()"_, se declararan variables como  _"option, j, numero, i, asteriscos"_  de tipo entero. 

El programa le muestra al usuario las 4 opciones para escoger y le pide que ingrese una opción del  1 al 4. Según el dato seleccionado por el usuario este se guarda en la variable: "option".  

Se utilizo  una estructura de control: "según" en la cual dependiendo de la opción que el usuario seleccione este se guardara en la variable "option" y se ejecutara el caso correspondiente. Dentro de cada caso se utilizo un ciclo "for" para generar el patrón del triangulo deseado.  

**Caso 1:** 
Utiliza dos bucles "for" anidados para generar un triángulo de arriba a derecha de asteriscos con la cantidad de filas especificada por el usuario. Cada fila tiene un asterisco más que la anterior, y esto se logra mediante el uso de dos bucles "for" que controlan el número de asteriscos impresos en cada fila.

**Caso 2:**
Genera un triángulo de asteriscos donde cada fila tiene un asterisco más que la anterior y se alinea hacia la derecha debido a la impresión de espacios en blanco antes de los asteriscos.

**Caso 3:**
Este caso genera un triángulo donde cada fila tiene un asterisco menos que la fila anterior.

**Caso 4:**
Este caso es similar al "Caso 3", pero agrega espacios en blanco antes de los asteriscos para que el triángulo tenga una alineación específica.

Abajo podrá encontrar el código fuente:

        //Triangulo Rectangulo
    #include <iostream>
    using namespace std;
    
    int main (){
    int option, j, numero, i, asteriscos;
    cout << "Ingrese una opcion" << endl;
    cout << "1. Triagulo arriba derecha" << endl;
    cout << "2. Triangulo arriba izquierda" << endl;
    cout << "3. Triangulo abajo derecha" << endl;
    cout << "4. Triangulo abajo izquierda" << endl;
    cin >> option;
    
    switch (option){
    	case 1:
    		int asteriscos;
        printf("Ingresa la cantidad de asteriscos para el triangulo: ");
        scanf("%d", &asteriscos);
        int i;
        for (i = 1; i <= asteriscos; i++)
        {
            int j;
            for (j = 0; j < i; j++)
            {
                printf("*");
            }
            printf("\n");
    		} 
    	case 2:
        printf("Ingresa la cantidad de asteriscos para el triangulo: ");
        scanf("%d", &asteriscos);
           for (i = asteriscos; i >= 1; i--) {
            // Imprimir espacios en blanco antes de los asteriscos
            for (j = 0; j < asteriscos - i; j++) {
                printf(" ");
            }
    
            // Imprimir los asteriscos
            for (j = 0; j < i; j++) {
                printf("*");
            }
    
            printf("\n");
        }
        case 3:
        printf("Ingresa la cantidad de asteriscos para el triangulo: ");
        scanf("%d", &asteriscos);
    
        for (i = asteriscos; i >= 1; i--) {
            for (j = 1; j <= i; j++) {
                printf("*");
            }
            printf("\n");
        }
        case 4:
        printf("Ingresa la cantidad de asteriscos para el triangulo: ");
        scanf("%d", &asteriscos);
    
        for (i = asteriscos; i >= 1; i--) {
            for (j = 0; j < asteriscos - i; j++) {
                printf(" ");
            }
            for (j = 0; j < i; j++) {
                printf("*");
            }
    
            printf("\n");
        }
    	return 0;
    	}	
    }
#
## Python

El programa comienza pidiendo al usuario que ingrese un número `n`. Luego, utiliza bucles "for" para generar cada secuencia de triángulos con base en el valor de `n`.

Este código es interactivo y versátil es mas simple que los anteriores ya que en este, se le permite al usuario elegir el número `n` y ver diferentes patrones de triángulos en una sola impresión. Es una forma práctica de explorar diferentes secuencias de triángulos de asteriscos en función de la entrada del usuario.

Secuencia 1: En esta secuencia, se genera un triángulo creciente de asteriscos en la esquina superior derecha. Cada fila tiene un asterisco más que la fila anterior.

Secuencia 2: En esta secuencia, se genera un triángulo creciente de asteriscos en la esquina superior izquierda. Se utilizan espacios en blanco para alinear el triángulo hacia la derecha. Cada fila tiene un asterisco más que la fila anterior.

Secuencia 3: En esta secuencia, se genera un triángulo decreciente de asteriscos en la esquina inferior derecha. Cada fila tiene un asterisco menos que la fila anterior.

Secuencia 4: En esta secuencia, se genera un triángulo decreciente de asteriscos en la esquina inferior izquierda. Se utilizan espacios en blanco para alinear el triángulo hacia la derecha. Cada fila tiene un asterisco menos que la fila anterior.

        #Triangulos 
    n = int(input("Ingrese un número para formar los triangulos: "))
    
    # Secuencia 1: arriba derecha
    print("Secuencia 1:")
    for i in range(1, n + 1):
        print('*' * i)
    
    # Secuencia 2: Triángulos arriba izquierda
    print("Secuencia 2:")
    for i in range(1, n + 1):
        print(' ' * (n - i) + '*' * i)
    
    # Secuencia 3: Triángulos abajo derecha
    print("Secuencia 3:")
    for i in range(n, 0, -1):
        print('*' * i)
    
    # Secuencia 4: Triángulos abajo izquierda
    print("Secuencia 4:")
    for i in range(n, 0, -1):
        print(' ' * (n - i) + '*' * i)
