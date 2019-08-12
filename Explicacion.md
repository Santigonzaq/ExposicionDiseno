# Patron de diseño Decorator

**Patron comportamental**
###Especializado para proporcionarle a los objetos funcionalidades extras en tiempo de ejecución, sin necesidad de moficar el código base.

## Elementos importantes:

### Component:
define la interfaz de los objetos a los que se les puede añadir responsabilidades dinámicamente (los objetos que quiero decorar).

### Decorator: 
Mantiene una referencia a un objeto Component (al que voy a decorar) y tiene su misma interfaz.

### ConcreteDecorator: 
añade responsabilidades al componente, en otras palabras, lo decora.

## USO:
### 1.
Se debe definir una interfaz o clase, la cual me va a representar las funcionalidades que los objetos que quiero decorar van a implementar.

### 2. 
Se debe crear la clase abstraca principal, la cual será el decorador. Esta clase también implementa la interfaz y adicionalmente, mantiene como atributo una referencia hacia la clase de los objetos que quiero decorar.

### 3.
Se debe crear la clase principal, la cual es la que representa los objetos que quiero decorar, esta clase también implementa la interfaz

### 4.
Posteriomente se crean las clases que extienden al decorador. Estas clases son las que añaden funcionalidades extra a los métodos definidos en la interfaz, así como también pueden agregar atributos.

### Forma de instanciar:
A la hora de instanciar, se encadenan recursivamente los llamados de la creación, según que funcionalidades extras (concreteDecorators) quiero establecer en nuevo objeto.
###Ejemplo:  
  **Widget widget =new BorderDecorator(new ScrollDecorator(new TextField(80, 24)));**
  #### ->Creando un objeto TextField, con las funcionalidades extendidas dadar por BorderDecorator y ScrollDecorator.
