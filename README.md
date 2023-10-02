# Hola mundo

![](https://i.blogs.es/5ff5c1/hello_world/1366_2000.webp)

Como tal al momento de iniciar y trabajar con un nuevo lenguaje de programacion o un nuevo entorno de desarrollo, es importanta saber que todo lo basico funciona de manera corrercta, uno de las mejores forma de trabajar en ello es usar el "hola mundo". El propósito principal de un programa "Hola Mundo" es demostrar cómo escribir, compilar y ejecutar un programa básico en un lenguaje de programación en particular o un entornor de desarrollo. 

# Codigo - Ejemplo repo interfaz
	"
	# Title: Hola mundo en ARM					Filename: holamundo.s
	# Author: ___________				Date: ___
	# Description: Mostrar HOLA MUNDO
	# Input: -
	# Output: HOLA MUNDO

	.global _start
	############################# Code segment ####################################
	_start:
  	MOV R7, #4 ###;- cargar el valor de datos que esta en esta posicion en la secuencia de instrucciones
  	MOV R0, #1 ###;- cargar el valor de datos que esta en esta posicion en la secuencia de instrucciones
  	MOV R2, #12 ###;- parametro
  	LDR R1, =string ###parametro y direccion de la cadena
  	SWI 0 ### señal de interrupcion al O.S.
  	MOV R7, #1 ### salir del programa y matar el proceso
  	SWI 0 ### señal de interrupcion al O.S. para la terminacion
	############################# Data segment ###################################
  	.data
	string:
 	.ascii "HOLA MUNDO" "

1.- En esta seccion se comenta informacion basica del codigo, como el titulo, descripcion y la salida.

	# Title: Hola mundo en ARM					Filename: holamundo.s
	# Author: ___________				Date: ___
	# Description: Mostrar HOLA MUNDO
	# Input: -
	# Output: HOLA MUNDO

2.- El codigo inicia a paratir de la palabra "_start:" es una etiqueta que marca el punto de entrada del programa.

 	############################# Code segment ####################################
	_start:

3.- En esta seccion se ejecunta un grupo de instrucciones:
MOV R7, #4: Carga el valor 4 en el registro R7, que corresponde a la llamada al sistema para escribir en la salida estándar (stdout).
MOV R0, #1: Carga el valor 1 en el registro R0, que es el descriptor de archivo para la salida estándar (stdout).
MOV R2, #12: Carga el valor 12 en el registro R2. Este valor se utiliza como parámetro para indicar la longitud de la cadena que se va a imprimir.
LDR R1, =string: Carga la dirección de la etiqueta string en el registro R1. Esto establece el puntero a la cadena que se va a imprimir.
SWI 0: Genera una señal de interrupción al sistema operativo (syscall) para realizar la escritura en la salida estándar. El sistema operativo procesará esta llamada y escribirá la cadena en la pantalla.

	MOV R7, #4 ###;- cargar el valor de datos que esta en esta posicion en la secuencia de instrucciones
	MOV R0, #1 ###;- cargar el valor de datos que esta en esta posicion en la secuencia de instrucciones
	MOV R2, #12 ###;- parametro
	LDR R1, =string ###parametro y direccion de la cadena
	SWI 0 ### señal de interrupcion al O.S.


4.- Instrucciones finales del programa:  
-MOV R7, #1: Carga el valor 1 en el registro R7, que corresponde a la llamada al sistema para salir del programa.
-SWI 0: Genera otra señal de interrupción al sistema operativo para finalizar el programa

	MOV R7, #1 ### salir del programa y matar el proceso
	SWI 0 ### señal de interrupcion al O.S. para la terminacion

 5.- Salida del hola mundo: La etiqueta string define una cadena de caracteres "HOLA MUNDO" en formato ASCII. Esta cadena se utiliza en el código para imprimir en la salida estándar.

 	############################# Data segment ###################################
  	.data
	string:
 	.ascii "HOLA MUNDO" "


# Torres de Hanoi
![](https://upload.wikimedia.org/wikipedia/commons/6/60/Tower_of_Hanoi_4.gif)

Las torres de Hanói es un rompecabezas matemático El propósito del rompecabezas es mover todos los discos a uno de los postes vacíos de forma que queden apilados preservando el orden inicial.

Suponiendo que todos los n discos estén distribuidos en disposiciones válidas entre las clavijas; suponiendo que hay m discos superiores en una clavija de origen y que el resto de los discos son más grandes que m , por lo que pueden ignorarse con seguridad; para mover m discos desde una clavija de origen a una clavija de destino usando una clavija de repuesto , sin violar las reglas:

1. Mueva m − 1 discos desde la fuente a la clavija de repuesto , mediante el mismo procedimiento de resolución general . Las reglas no se violan por suposición. Esto deja al disco m como disco superior en la clavija de origen.
2. Mueva el disco m desde la clavija de origen a la de destino , lo que se garantiza que será un movimiento válido, según las suposiciones: un paso simple .
3. Mueva los m − 1 discos que acabamos de colocar en el disco de repuesto, desde el repuesto hasta la clavija de destino mediante el mismo procedimiento de resolución general , de modo que queden colocados encima del disco m sin violar las reglas.
4. El caso base es mover 0 discos (en los pasos 1 y 3), es decir, no hacer nada, lo que obviamente no viola las reglas.

La solución completa de la Torre de Hanoi consiste entonces en mover n discos desde la clavija de origen A a la clavija de destino C, utilizando B como clavija de repuesto.



# Código del programa

En esta sección, se declarán los datos necesarios. el nombre de los Peg debe ser un carácter. n = 4, es el número de discos a mover.

![image](https://github.com/tectijuana/armexpos-covid/assets/105743084/9eee297f-3cf0-4427-9108-2987879c1b58)


Declarar un método con los parámetros n, Source, Dest, Extra) y abrir una condición que evalúe que disco mover y hacia que lugar.

![image](https://github.com/tectijuana/armexpos-covid/assets/105743084/c87a23e7-305a-4b48-963e-f6685261dc36)

![image](https://github.com/tectijuana/armexpos-covid/assets/105743084/de229cbf-4a3c-4d70-beb0-dd097a9a2fb2)

![image](https://github.com/tectijuana/armexpos-covid/assets/105743084/fb59efaa-0c47-4785-94ea-ec713f12744d)


# Ejecución del programa

![image](https://github.com/tectijuana/armexpos-covid/assets/105743084/57e0c777-a0d9-4398-8b6f-5ef7d1a9b2fe)


# Dividir 9 entre 3

![image](https://github.com/tectijuana/armexpos-covid/assets/105743084/854b16e2-e1ef-41da-b313-9666943f9b0d)

  
# Ejecución del programa

![image](https://github.com/tectijuana/armexpos-covid/assets/105743084/ac7f27d2-9434-4f31-9ed5-729692bd662c)


# Media aritmetica

_Obtiene la media aritmetica de 5 pares de valores (truncado a enteros)_

``` @ DATA SECTION ```

``` .data ```

``` string: 	.asciz	  "%d\n" ```

``` @ CODE SECTION ```

``` .text ```

``` .extern printf ```

``` .global main ```

``` main: ```

	@ primera ...
 
	push	{r0, r1}	@ almacenamiento de valores iniciales
	mov 	r0, #3
	mov 	r1, #2
	add 	r2, r0, r1	@ (r0+r1)
	mov 	r2, r2, LSR #1	@ (r0+r1)/2
	mov 	r1, r2		@ impresion del resultado...
	ldr 	r0, =string
	bl	printf

	@ segunda ...
        mov     r0, #4
        mov     r1, #6
        add     r2, r0, r1
        mov     r2, r2, LSR #1
        mov     r1, r2
        ldr     r0, =string
        bl      printf

	@ tercera ...
        mov     r0, #7
        mov     r1, #2
        add     r2, r0, r1
        mov     r2, r2, LSR #1
        mov     r1, r2
        ldr     r0, =string
        bl      printf

	@ cuarta ...
        mov     r0, #0
        mov     r1, #3
        add     r2, r0, r1
        mov     r2, r2, LSR #1
        mov     r1, r2
        ldr     r0, =string
        bl      printf

	@ quinta ...
        mov     r0, #3
        mov     r1, #5
        add     r2, r0, r1
        mov     r2, r2, LSR #1
        mov     r1, r2
        ldr     r0, =string
        bl      printf
	pop	{r0, r1}	@ recuperacion de estados iniciales para salir
	bx	lr		@ BREAK

# Ejecución del programa

![image](https://github.com/tectijuana/armexpos-covid/assets/105743084/616cfd8b-aa87-4ab4-a3bb-b7dd7a23f16c)

# Uso de la función C scanf () para la entrada del usuario

La función scanf se utiliza comúnmente para leer diferentes tipos de datos, como números enteros, números en punto flotante, caracteres y cadenas de caracteres, siguiendo un formato específico. 
**Sección de Datos:**
Comencemos por la sección de datos de nuestro código. En esta parte, definimos algunas cadenas y una variable que serán fundamentales para nuestro programa. La cadena "prompt" contiene el mensaje que se mostrará al usuario antes de que ingresen un número. La cadena "format" especifica cómo se debe leer el número (en este caso, como un entero %d). La variable num almacenará el número ingresado por el usuario, y la cadena "output" es el formato de salida que utilizaremos para mostrar el número ingresado.
	
 	.data
	.balign 4
	prompt: .asciz "Ingrese Datos> "
	format: .asciz "%d"
	num: .int 0
	output: .asciz "Tu entrada: %d\n"
 
**Sección de Código:**

	.text
	.global main
	.extern printf
	.extern scanf
	
	main: push {ip, lr} @ guardar la dirección de retorno + registro ficticio
	                   @ para alineación
1. Inicio de la función main: Iniciamos la función main y guardamos la dirección de retorno junto con un registro ficticio para asegurarnos de que todo esté alineado correctamente.

		ldr r0, =prompt @ imprimir el mensaje de entrada
		bl printf

2. Mostrar el mensaje de entrada: Utilizamos la función printf() para mostrar el mensaje " > " al usuario. Esto es lo que verán antes de ingresar su número.
   
		ldr r0, =format @ llamar a scanf, y pasar la dirección del formato
		ldr r1, =num    @ y la dirección de num en r0, y r1, respectivamente,
		bl scanf        @ respectivamente.

3. Lectura del número: Aquí es donde entra en juego scanf(). Cargamos la dirección de la cadena de formato "format" en r0 y la dirección de la variable num en r1. Luego, llamamos a scanf(). Espera a que el usuario ingrese un número y lo almacena en la variable num.
 
		ldr r1, =num    @ imprimir num formateado con la cadena de salida.
		ldr r1, [r1]
		ldr r0, =output
		bl printf

4. Mostrar el número ingresado: Ahora que tenemos el número en num, necesitamos mostrarlo al usuario. Para hacerlo, cargamos la dirección de num en r1, leemos su contenido y lo almacenamos en r1. Luego, cargamos la dirección de la cadena "output" en r0 y llamamos a printf(). Como resultado, el número ingresado se mostrará en la pantalla en el formato deseado.
 
		pop {ip, pc}    @ recuperar la dirección de retorno en pc

5. Fin de la función main: Finalmente, recuperamos la dirección de retorno y salimos de la función main.
