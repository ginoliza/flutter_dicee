# Dicee flutter
## `Expanded` [widget]
Solo un hijo, este hijo llena el espacio disponible en pantalla, tamaño automatico de multiples **Expanded**. 

### `flex` [prop]
Es como el ratio de bootstrap, determina la proporcion de los **Extended**

## `Image.asset` [widget] 
Es la manera mas corta para no tener que escribir `Image(image: AssetImage())`
Funciona tambien para `Image.network` en vez de `Image(image: NetworkImage())`

## Flutter outline
Es una utilidad de flutter para poder realizar acciones mas rapidamente, como centrar.

## Detectar acciones con `TextButton` [widget]
Viene por defecto con padding a los lados, se requiere un void callback, `onPressed: () {}` [propiedad] que  necesita una funcion anonima, podemos poner dentro de las llaves `print('button got pressed')` para saber que realmente funciona cuando se presiona el botón.

## Funciones 
Se puede declarar asi:
```
void buttonGotPressed() {
    print('button got pressed from function');
}
```
Y  llamarla en cualquier lado con `buttonGotPressed();` 

## Interpolacion de strings
Usando `$` podemos insertar una variable dinamicamente en un string
```
var leftDiceNumber = 5;
child: Image.asset('images/dice$leftDiceNumber.png')
```
Es importante recordar que si queremos que la imagen se actualice, la variable debe estar dentro del `build`

## Variables
No se puede cambiar los tipos ya que **dart** es un lenguaje estaticamente tipado
```
var myName = 'Gino';
myName = 123;
```

## Tipos de datos
**Primitivos** <br>
```
string a = "asd";
int b = 12; 
double c = 6.9;
bool d = false;
```
**Dinamico** <br>
```
dynamic a = 12;
a = 'asd';
a = 10.2;
```
**var** es puede ser dinamico tambien, pero solo si no se asigna un valor inicial. <br>
Es mejor evitar estos tipos

## Stateful widgets
Cambiamos a un `stateful widget` debido a que los `stateless widgets` no deeb realmente cambiar. <br>
Se puede usar `stful` como emmet de android studio, o podemos simplemente convertir nuestro `stateless widget` a `stful`. <br>
Ahora dentro de `onpressed(){}` debemos poner `setState(() { leftDiceNumber = 1; }` para cambiar el estado del widget. Esto porque `setState` llama al build del widget. Si no llamamos a `setState` cambiará todo menos la vista.

## Numeros aleatorios
Incluir la libreria 
`dart:math`
Y para usarlo
```
leftDiceNumber = Random().nextInt(6) + 1; // [1-6] 
```