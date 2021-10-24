# ETS

## 1. CALCULO DE ÁREAS

Queremos crear una aplicación para calcular el área de las siguientes figuras:

![](images/1.png)

Para ello empezaremos creando un menú, para facilitar al usuario la elección de la figura. En el menú incluiremos los nombres de todas las figuras, de la siguiente manera:
````
/* **Elige una figura:**
- 1. Triangulo.
- 2. Cuadrado.
- 3. Rectángulo.
- 4. Rombo.
- 5. Romboide.
- 6. Trapecio.
- 7. Pentágono.
- 8. Circulo.
- 9. Salir.
*/
````
Ahora pasaremos a lo que incluiremos en cada clase de figura, indicando al usuario los datos que necesitaremos a la hora de hacer los cálculos, junto con la clase `Salir`.

```
/* class Triangulo

“Introduce base”
b=

“Introduce altura”
h=

“El área es:”
area=(b*h)/2
````

*Cada vez que el usuario termine un calculo, se le mostrará de nuevo el menú principal, para ue escoja si quiere salir o si va a realizar otro calculo.*

````
/* class Cuadrado

“Introduce lado”
l=

“El área es:”
area=l*l
````

````
/* class Rectangulo

“Introduce base”
b=

“Introduce altura”
h=

“El área es:”
area=b*h
````
````
/* class Rombo

“Introduce diagonal 1”
d=

“Introduce diagonal 2”
D=

“El área es:”
area=(D*d)/2
````

````
/* class Romboide
“Introduce base”
b=

“Introduce altura”
h=

“El área es:”
area=b*h
````

````
/* class Trapecio

“Introduce base 1”
b=

“Introduce base 2”
B=

“Introduce altura”
h=

“El área es:”
area=((b*B)/2)*h
````
````
/* class Pentagono

“Introduce perímetro”
P=

“Introduce apotema”
a=

“El área es:”
area=(P*a)/2
````

````
/* class Círculo

“Introduce radio”
r=

“El área es:”
area=2*π*r
````
