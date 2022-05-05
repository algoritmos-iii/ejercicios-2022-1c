# Números

## Primera parte

Hacer file-in del archivo Numeros-Parte1-Ejercicio.st.

Como se observa, contamos con una clase Numero que representa un modelo de números. En particular soporta operaciones de enteros y de fracciones.
Contamos con una suite de tests que verifica una serie de operaciones básicas que soporta nuestro modelo.

El objetivo de esta primera parte es quitar los ifs utilizando polimorfismo, aplicando el algoritmo que vimos en clase. 

Los tests deben seguir pasando (sin modificarlos).

## Preguntas teóricas

### Aporte de los mensajes de DD
En un double dispatch, ¿qué información aporta cada uno de los dos llamados?

### Lógica de instanciado
Con lo que vieron y saben hasta ahora, ¿donde les parece mejor tener la lógica de cómo instanciar un objeto? ¿por qué? ¿y si se crea ese objeto desde diferentes lugares y de diferentes formas? ¿cómo lo resuelven?

### Nombres de las categorías de métodos
Con lo que vieron y trabajaron hasta ahora, ¿qué criterio están usando para categorizar métodos?

### Subclass Responsibility
Si todas las subclases saben responder un mismo mensaje, ¿por qué ponemos ese mensaje sólo con un “self subclassResponsibility” en la superclase? ¿para qué sirve?

### No rompas
¿Por qué está mal/qué problemas trae romper encapsulamiento?
