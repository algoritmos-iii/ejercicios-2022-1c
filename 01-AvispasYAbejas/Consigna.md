# Enunciado

Vamos a continuar trabajando con las avispas. En esta ocasión debemos dar el soporte para que nuestro cliente pueda determinar cuándo una avispa se reproduce, definir líneas genéticas y cantidad de recursos en el hábitat.

## Las orugas de Oriana y Ornella
El objetivo de las avispas es intentar reproducirse, es decir poner un huevo. Pero únicamente dejan un huevo si logran obtener del hábitat alimento para que la futura descendiente al nacer pueda nutrirse. 
 
Debemos modelar dos avispas Oriana y Ornella que con cada uno de sus huevos le dejan una oruga para que sus herederas se alimenten, pero cuando no logran conseguir ninguna oruga no ponen ningún huevo.

## Las polillas de Polly

Nuestro cliente también nos pide poder manipular otra avispa que se comporta de forma similar a las anteriores pero en lugar de obtener orugas para que se alimenten sus descendientes debe conseguir polillas. 

Nuestro trabajo es modelar a la avispa Polly que se comporte de forma similar a Oriana y Ornella pero que sus presas sean polillas en lugar de orugas.

## Trascender 

Las avispas pertenecen a una línea genética, la cual es legada a sus huevos. Debemos modificar nuestro modelo para que tanto Oriana, Ornella y Polly al poner huevos estos tengan las firmas genéticas de su progenitora. Un dato importante, es que Oriana y Ornella tienen la misma firma genética, sin embargo Polly tiene una firma diferente.
Lara la avispa ladrona

El experto en el dominio nos contó que existen avispas que en vez de cazar orugas o polillas, le roba el nido a otra avispa y lo reemplaza por el suyo. Debemos modelar a la Avispa Lara que al intentar reproducirse proceda de esta forma. Lara tiene una firma genética diferente a las de las avispas anteriores.

# Punto de partida

Deben importar el código inicial Ejercicio1-Avispas-y-Abejas-Episodio2.CodigoInicial.st y construir su solución a partir de ahí. En dicho paquete encontrarán al objeto PruebasReproduccionDeAvispas que agrupa las pruebas de funcionamiento de las avispas. El objetivo de estas pruebas es ayudarlos/as a implementar lo pedido. En ellas encontrarán que tienen que implementar algunos métodos para poder completar las pruebas.

**Sugerencias:** 

Vayan haciendo pasar las pruebas según el orden estipulado en su numeración. 

#Preguntas para después de hacer el ejercicio

A continuación les planteamos algunas cuestiones para pensar y contestar.
Las preguntas van a ser evaluadas también.

## Sobre implementar funcionalidad

 Los tests 01, 02 y 03 demuestran la funcionalidad de cómo se incrementa la cantidad de huevos de avispas a medida que los van dejando. Cuando los implementaste, ¿esos tests pasaron (los tres) de una?
¿podrías haber implementado esta funcionalidad de a partes, haciendo que pase el 01, luego el 01 y el 02 y por último el 01, 02 y 03? ¿se te ocurre cómo?
Y si lograste hacerlo, ¿qué pensas de implementar esa funcionalidad de esa forma?

## Sobre código repetido

¿les quedó código repetido? ¿dónde? ¿Se animan a adivinar qué cosa del dominio les faltó representar (y por eso tienen código repetido)?
Responsabilidad de dejar un huevo consumiendo otro insecto
¿Quién les quedó, en su modelo, que es el responsable de ver si hay suficientes polillas u orugas y entonces dejar un huevo? ¿el insecto (Polly, Oriana, etc) o el hábitat?
¿por qué? ¿por qué tendría sentido que fuera de la otra forma? ¿con cuál nos quedamos?

## Sobre código repetido 2

Con lo que vimos en la clase del Jueves (en la parte teórica, prototipos vs clases) ¿cómo sacarían este código?
Sobre la implementación
¿cómo resolvieron guardar los huevos?
¿Usaron colecciones? ¿Diccionarios? ¿Uno, varios? ¿con qué indexaban?
Pero la pregunta más importante:
¿es lo más sencillo que hacía falta? ¿o se podía hacer menos y todo andaba?


# Tips

**¿Cómo crear un diccionario?**

```smalltalk
unDiccionario := Dictionary new.
```

**¿Cómo asociarle una clave y un valor a un diccionario?**

```smalltalk
unDiccionario := Dictionary new.
unDiccionario at: ‘unaClave’ put:  ‘unValor’
```

**¿Cómo acceder al valor de una clave o a un valor por defecto si el diccionario no contiene dicha clave?**

```smalltalk
unDiccionario := Dictionary new.
unDiccionario at: ‘unaClave’ ifAbsent: [ ‘unValorPorDefecto’ ]
```

**¿Cómo acceder a las claves de un diccionario?**

```smalltalk
unDiccionario := Dictionary new.
unDiccionario keys
```
 
**¿Cómo acceder a todos los valores asociados de un diccionario?**

```smalltalk
unDiccionario := Dictionary new.
unDiccionario values
```
**¿Cómo sumar una colección de números?**

```smalltalk
unaColeccion := #(1 2 3 4 5).
unaColeccion sum: [ : unNumero | unNumero ] ifEmpty: [ 0 ]
```
 
**¿Cómo evaluar unas colaboraciones u otras según un objeto booleano?**

```smalltalk
unBooleano ifTrue: [ “envios de mensajes para cuando unBooleano es true” ] ifFalse: [ “envios de mensajes para cuando unBooleano es false”  ]
```

