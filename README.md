# Introducción

# Parte I: Traslación y Rotación del personaje en C#

## Antes de trabajar en los movimientos del personaje en C#, comenzamos el proyecto importando el paquete _Robot Hero: PBR HP Polyart_. Insertamos la figura _PolyartCharacter_, encontrada en la carpete de Prefabs; llamemos al robot (insertar nombre) por la duración el proyecto.

![image](https://github.com/user-attachments/assets/56f09a0e-0637-48fe-9897-f8961d2c4f15)

## No queremos que (insertar nombre) quede flotando en la nada, por lo tanto, colocamos un terreno de 40 metros de ancho y 40 metros de largo, ajustando la altura a 50 metros. Más adelante, haremos algunos detalles con el terreno.

![image](https://github.com/user-attachments/assets/18be7896-c39f-46ec-b49e-90050981104b)

## Para permitir que (insertar nombre) se mueva en C#, añadimos el componente de Script, lo nombramos _Player_Movement_ y procedemos a editarlo en Visual Studio Code. 

![image](https://github.com/user-attachments/assets/53593a7c-27e6-4eef-ab68-3b2e510a3a2c)
![image](https://github.com/user-attachments/assets/e7e8fcaa-80cd-4aa8-9821-2e402860cb1f)

## En el script comenzamos integrando la traslación con las teclas WASD o las flechas del teclado ⬆️⬇️⬅️➡️. Primero declaramos una variable pública de tipo float llamada speed. Hacerla pública nos permitirá editarla en el Inspector del proyecto. A continuación, insertamos las condiciones IF-Else para determinar la dirección del personaje. Esto es suficiente para que (nombre) se mueva:

![image](https://github.com/user-attachments/assets/0da02be8-e976-461e-9228-b46a49aa171b)

## Una vez hecho esto, añadimos la rotación del personaje utilizando el mouse. Declaramos otra variable pública de tipo float llamada speedRotation. Después de las condiciones IF-Else, colocamos la línea de código que permite la rotación. Además, al eliminar los else, logramos que el personaje se mueva en direcciones diagonales. A continuación mostraremos el código completo y un video de demostración.

![image](https://github.com/user-attachments/assets/8b52e82e-bae9-41ea-93e1-646e75d2c866)
https://github.com/user-attachments/assets/a4492d3e-9648-45d6-8149-78cda61c9192


# Parte II: Traslación y Rotación del personaje en Visual Graph
