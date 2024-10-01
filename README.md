# Introducción

# Parte I: Rotacion del personaje en C#
## 

## Antes de trabajar en los movimientos del personaje en C#, comenzamos el proyecto importando el paquete de _Robot Hero: PBR HP Polyart_ que hemos utilizado previamente. Insertamos la figura PolyartCharacter, el cual llamaremos (insert nombre) por el resto del proyecto.

(Primera foto)

## Para no dejar el pobre (insert nombre) flotando en la nada, colocamos un terreno sobre el. El terreno tiene una anchura de 40 metros y un largo de 40 metros. Se ajusto la altura a 50 metros. Mas adelante haremos unos detalles con el terreno. 

(Segunda foto)

## Para hacer que  (insert nombre) se mueva en C#, anadimos el component de Script, lo llamamos _Player_Movement_ y proseguimos a Visual Studio Code para editarlo.

![image](https://github.com/user-attachments/assets/9af03085-6f84-408a-a9be-2b72c2f0ff44)

## Para anadir movimiento en las teclas WASD o las flechas ⬆️⬇️⬅️➡️ del teclado primero declaramos 
una variable publica de tipo float llamada speed. Hacerla publica nos permite editarla en el Inspector del proyecto como tal. Proseguimos a insertar las condiciones _IF_Else_ para determinar la direccion del personaje.

foto

## Una vez hecho, lo que quedaria seria la rotacion del personaje con el mouse. Declaramos otra variable publica de tipo float llamada _speedRotation_ y, despues de las condiciones ifelse, colocamos la linea de codigo que permite que ocurra dicha rotacion. Ademas, logramos hacer que el personaje se mueva en direcciones diagonales removiendo los else de las condiciones:


## Aqui queda el resultado del script en video:


https://github.com/user-attachments/assets/ce91e3cd-e07d-4c4e-aa8d-78f8ae6a62cd




# Parte II: Rotacion del personaje en visual graph
