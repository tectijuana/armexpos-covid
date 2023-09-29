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

.global main

.func main

.arm

main:    	  ADR R5, thumbcode+1     //se asigna la dirección de la etiqueta thumbcode al registro 5

		  MOV LR, PC              //se almacena la siguiente instrucción en el registro LR
  
		  BX R5                   //salto al registro r5

exit:   	  MOV R0, R3

		  MOV R7, #1
  
		  SWI 0

.thumb

thumbcode:    	  MOV R0, #9     //Se almacena el valor del numerador

		  MOV R1, #3     //Se almacena el valor del denominador
  
		  MOV R3, #0     //Se utiliza como contador para saber cuantas veces cabe
		
loop:    	  ADD R3, #1    //Se aumenta el contador en 1

		  SUB R0, R1    //Se resta valor del denominador al valor del numerador
  
		  BGE loop      //Se preguna se el resultado es un valor mayor o igual
  
		  SUB R3, #1    //Resultado de la división
  
		  BX LR	      //Retorno a al código principal
  
# Ejecución del programa

![image](https://github.com/tectijuana/armexpos-covid/assets/105743084/ac7f27d2-9434-4f31-9ed5-729692bd662c)

