# Bullet Time

# Introducción:

## El objetivo principal de esta actividad es repasar varios conceptos dados en clase que son primordiales para la creación de videojuegos. Estos conceptos consisten en los primeros inputs que daremos a nuestro personaje junto con la implementación de disparar balas. 

# Parte I: Traslación y Rotación del Personaje en C#

## Antes de trabajar en los movimientos del personaje en C#, comenzamos el proyecto importando el paquete _Robot Hero: PBR HP Polyart_. Insertamos la figura _PolyartCharacter_, encontrada en la carpete de Prefabs.

![image](https://github.com/user-attachments/assets/71a23901-4f7b-4dcb-8ae1-5ad152da8482)

## No queremos que el pobre robot quede flotando en la nada, por lo tanto, colocamos un terreno de 40 metros de ancho y 40 metros de largo, ajustando la altura a 50 metros. Más adelante, haremos algunos detalles con el terreno.

![image](https://github.com/user-attachments/assets/18be7896-c39f-46ec-b49e-90050981104b)

## Para permitir que nuestro personaje se mueva en C#, añadimos el componente de Script, lo nombramos _Player_Movement_ y procedemos a editarlo en Visual Studio Code. 

![image](https://github.com/user-attachments/assets/53593a7c-27e6-4eef-ab68-3b2e510a3a2c)

## En el script comenzamos integrando la traslación con las teclas WASD o las flechas del teclado ⬆️⬇️⬅️➡️. Primero declaramos una variable pública de tipo float llamada speed. Hacerla pública nos permitirá editarla en el Inspector del proyecto. A continuación, insertamos las condiciones IF-Else para determinar la dirección del personaje. Esto es suficiente para que el personaje se mueva:

![image](https://github.com/user-attachments/assets/0da02be8-e976-461e-9228-b46a49aa171b)

## Una vez hecho esto, añadimos la rotación del personaje utilizando el Mouse. Declaramos otra variable pública de tipo float llamada speedRotation. Después de las condiciones IF-Else, colocamos la línea de código que permite la rotación. Además, al eliminar los else, logramos que el personaje se mueva en direcciones diagonales. Finalmente, incluimos una funcioó nueva llamada _Start_ que se encaraga de esconder el cursor durante la ejecución del programa. A continuación mostraremos el código completo y un video de demostración.

![image](https://github.com/user-attachments/assets/7a995b04-bd82-46c7-9118-6791341bbea5)
https://github.com/user-attachments/assets/d998968b-aa96-46fd-8ce8-432d611fde7b



# Parte II: Traslación y Rotación del Personaje en Visual Graph

## Para mover al robot mediante Visual Graph, comenzamos insertando un nuevo script tipo machine (graph) en el personaje. Es crucial desactivar el script de movimiento en C# para evitar conflictos al mover el personaje con el nuevo script.

![image](https://github.com/user-attachments/assets/06330141-f475-40ae-8fc2-c842e479db8d)

https://github.com/user-attachments/assets/7afecae9-8db8-4250-be81-df47784fcba2


## A continuación, seguimos el diagrama para agregar los bloques de movimiento. El siguiente conjunto de nodos permite que el robot avance con la tecla W o la flecha ↑. Su funcionamiento es el siguiente:
##  - En cada _Update_ (frame), el nodo _Transform_Translate_ recibe el valor de una variable llamada speed, que controla la velocidad del robot (ajustable) en el eje Z, junto con el input de las teclas W o ↑.
##  - Ambos inputs están conectados mediante un OR, determinando cuál está siendo presionado. Con uno de los dos es suficiente para que el personaje se mueva.

![image](https://github.com/user-attachments/assets/da4c6453-6c42-4eb1-a6d2-c111ec3ef741)

## Para retroceder en el eje Z, cambiamos los inputs a S o ↓ y añadimos un nodo de multiplicación que invierte el valor, logrando así un movimiento en dirección opuesta en el eje Z. Conectamos este conjunto de nodos con el anterior          mediante un IF.

![image](https://github.com/user-attachments/assets/f82da8e0-e309-493f-ae48-069da74a5124)

## Repetimos este proceso para el eje X, modificando los inputs del nodo _Transform_Translate_ para que afecten dicho eje.

![image](https://github.com/user-attachments/assets/3532bb2f-4026-4f0e-ab05-69eee4c6a5c7)

## Para romper los IF anidados, añadimos un nodo de secuencias que conecta todos los conjuntos.

![image](https://github.com/user-attachments/assets/be015ba5-262f-4029-b0e3-a8ec1ad83e82)

## El último conjunto de nodos controla la rotación del personaje en el eje Y con el mouse, utilizando un nodo Transform_Rotate similar a los anteriores, permitiendo así la rotación del robot.

![image](https://github.com/user-attachments/assets/81a02e74-4ec9-4d9a-b2fe-fe612a6f7fdf)

## Demostración del robot moviéndose con _Visual Graph_:

https://github.com/user-attachments/assets/9a0cf2e6-6644-4eb4-ae52-0e66be5bbaf6

# Parte III: Creacion del Prefab de la Bala

# Parte IV: Disparar la Bala en C#

# Parte V: Disparar la Bala en Visual Graph

# Parte VI: Algunos Detalles Adicionales: 
## Dado que la actividad se enfoca en disparar balas, ajustamos el terreno para que asemeje una zona de combate. Primero, cavamos una trinchera alrededor del perímetro y aplicamos una textura de fuego, simulando una arena. Usamos también una textura de piedra, que complementa la de fuego. Agregamos montañas para dar mayor robustez al terreno. Finalmente, incluimos copias del robot, llamadas enemy, para que parezca que nuestro protagonista luchará contra ellos.

# Parte VI: Opiniones Acerca del Proyecto

## Sebatián Negrón:
## Aunque en clase ya habíamos trabajado varios de estos ejercicios, fue muy útil enfocarnos en ellos nuevamente, ya que esta práctica nos dio la primera sensación real de estar creando un videojuego. A pesar de que los proyectos anteriores también fueron entretenidos, se sentían más como maquetas. Este proyecto fue diferente, ya que interactuamos directamente con el mundo creado. Además, me ayudó a mejorar en el uso de Visual Graph, que al principio me costó entender en clase.

## Mayra Lago

## Jancarlos González

