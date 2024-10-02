# Bullet Time

# Introducción

# Parte I: Traslación y Rotación del Personaje en C#

## Antes de trabajar en los movimientos del personaje en C#, comenzamos el proyecto importando el paquete _Robot Hero: PBR HP Polyart_. Insertamos la figura _PolyartCharacter_, encontrada en la carpete de Prefabs; llamemos al robot (insertar nombre) por la duración el proyecto.

![image](https://github.com/user-attachments/assets/71a23901-4f7b-4dcb-8ae1-5ad152da8482)

## No queremos que (insertar nombre) quede flotando en la nada, por lo tanto, colocamos un terreno de 40 metros de ancho y 40 metros de largo, ajustando la altura a 50 metros. Más adelante, haremos algunos detalles con el terreno.

![image](https://github.com/user-attachments/assets/18be7896-c39f-46ec-b49e-90050981104b)

## Para permitir que (insertar nombre) se mueva en C#, añadimos el componente de Script, lo nombramos _Player_Movement_ y procedemos a editarlo en Visual Studio Code. 

![image](https://github.com/user-attachments/assets/53593a7c-27e6-4eef-ab68-3b2e510a3a2c)
![image](https://github.com/user-attachments/assets/e7e8fcaa-80cd-4aa8-9821-2e402860cb1f)

## En el script comenzamos integrando la traslación con las teclas WASD o las flechas del teclado ⬆️⬇️⬅️➡️. Primero declaramos una variable pública de tipo float llamada speed. Hacerla pública nos permitirá editarla en el Inspector del proyecto. A continuación, insertamos las condiciones IF-Else para determinar la dirección del personaje. Esto es suficiente para que (nombre) se mueva:

![image](https://github.com/user-attachments/assets/0da02be8-e976-461e-9228-b46a49aa171b)

## Una vez hecho esto, añadimos la rotación del personaje utilizando el mouse. Declaramos otra variable pública de tipo float llamada speedRotation. Después de las condiciones IF-Else, colocamos la línea de código que permite la rotación. Además, al eliminar los else, logramos que el personaje se mueva en direcciones diagonales. A continuación mostraremos el código completo y un video de demostración.

![image](https://github.com/user-attachments/assets/8b52e82e-bae9-41ea-93e1-646e75d2c866)

https://github.com/user-attachments/assets/301a043c-44e6-43ba-976d-23634a642069

# Parte II: Traslación y Rotación del Personaje en Visual Graph

## Para mover al robot mediante Visual Graph, comenzamos insertando un nuevo script tipo machine (graph) en el personaje. Es crucial desactivar el script de movimiento en C# para evitar conflictos al mover el personaje con el nuevo script.

![image](https://github.com/user-attachments/assets/06330141-f475-40ae-8fc2-c842e479db8d)

## A continuación, seguimos el diagrama para agregar los bloques de movimiento. El siguiente conjunto de nodos permite que el robot avance con la tecla W o la flecha ↑. Su funcionamiento es el siguiente:
##  - En cada _Update_ (frame), el nodo _Transform_Translate_ recibe el valor de una variable llamada speed, que controla la velocidad del robot (ajustable) en el eje Z, junto con el input de las teclas W o ↑.
##  - Ambos inputs están conectados mediante un OR, determinando cuál está siendo presionado. Con uno de los dos es suficiente para que el personaje se mueva.

![image](https://github.com/user-attachments/assets/5e1e4b6c-1199-4168-afcf-c7bb1b21ce62)

## Para retroceder en el eje Z, cambiamos los inputs a S o ↓ y añadimos un nodo de multiplicación que invierte el valor, logrando así un movimiento en dirección opuesta en el eje Z. Conectamos este conjunto de nodos con el anterior          mediante un IF.


Repetimos este proceso para el eje X, modificando los inputs del nodo Transform para que afecten dicho eje.

Para romper los IF anidados, añadimos un nodo de secuencias que conecta todos los conjuntos.

El último conjunto de nodos controla la rotación del personaje en el eje Y con el mouse, utilizando un nodo Transform_Rotate similar a los anteriores, permitiendo así la rotación del robot.
  

https://github.com/user-attachments/assets/9a0cf2e6-6644-4eb4-ae52-0e66be5bbaf6

# Parte III: Creacion del Prefab de la Bala

# Parte IV: Disparar la Bala en C#

# Parte V: DIsparar la Bala en Visual Graph

# Parte VI: Opiniones Acerca del Proyecto

## Sebatián Negrón:

## Mayra Lago

## Jancarlos González

