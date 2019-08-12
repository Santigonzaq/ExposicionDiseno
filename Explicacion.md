# Patron de diseño Decorator

**Patron comportamental**
###Especializado para proporcionarle a los objetos funcionalidades extras en tiempo de ejecución, sin necesidad de moficar el código base.

## Elementos importantes:

### Component:
define la interfaz de los objetos a los que se les puede añadir responsabilidades dinámicamente (los objetos que quiero decorar).

### Decorator: 
Mantiene una referencia a un objeto Component (al que voy a decorar) y tiene su misma interfaz.

## ConcreteDecorator: 
añade responsabilidades al componente, en otras palabras, lo decora.


