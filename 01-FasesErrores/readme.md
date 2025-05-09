# TP #1: "Fases de la Traducción y Errores"

### Autor de la resolución:
```
 ◦ Juuan479

 ◦ 213.730-6

 ◦ Garcia

 ◦ Juan Ignacio
```
### Enunciado:
```
7.1. Objetivos

  • Este trabajo tiene como objetivo identificar las fases del proceso de traducción o Build y los posibles errores asociados a cada fase.

  • Para lograr esa identificación se ejecutan las fases de traducción una a una, se detectan y corrigen errores, y se registran las conclusiones.
```
### Resolución:
#### Preprocesador
```
b) Al preprocesar el archivo hello2.c, se genera el archivo hello2.i, donde se observa que los comentarios del tipo /* ... */ son eliminados completamente. Esto demuestra que el preprocesador no valida errores de sintaxis y simplemente elimina comentarios, expande macros y directivas como #include.

d) La primera linea declara manualmente el prototipo de la funcion printf, especificando que recibe un puntero a una cadena constante, seguido de una lista de argumentos variables. El modificador restrict indica que el puntero s es el unico que accedera a ese bloque de memoria, permitiendo posibles optimizaciones. Esta declaracion permite usar printf sin incluir biblioteca <stdio.h>

e) Al preprocesar hello3.c y generar hello3.i, se observa que no hay cambios significativos en el codigo, salvo las lineas de control del preprocesador. Esto ocurre porque no se utilizaron directivas como #incluide. Por lo tanto el preprocesador no realiza modificaciones si no tiene intrucciones especificas para ejecutar.

```
### Compilación
```

c) El objetivo de este código ensamblador es imprimir en pantalla el número 42 usando el formato "La respuesta es %d\n"

```
### Remoción de prototipo
```
b)
  i) El codigo va a arrojar un error por la simple razon que la funcion prinft no esta definida en ninguna parte del codigo, ya que no se cuenta con la biblioteca <stdio.h>
  ii) Un prototipo es una declaracion previa de una funcion que especifica su nombre, tipo de entorno y los tipos de sus parametros, generandola tanto manualmente en la parte superior del main o mediante archivos .h 
  iii) Una declaracion implícita de una función ocurre cuando una función es llamada es llamada sin haner sido previamente declarada mediante un prototipo o una definición antes de su uso
  iv) La especificación se refiere generalmente a la información completa sobre cómo debe utilizarse una función. Es decir, qué hace, qué parámetros necesita, qué tipo de dato retorna y bajo qué condiciones opera
  v) Las principales implementaciones buscan ajustarse al estandar del lenguaje, pero presentan diferencias en compatibilidad, rendimiento, herramientas diagnósticas y portabilidad.
  vi) Una función built-in es una función proporcionada por el compilador, no definida por el programador ni necesariamente parte de la biblioteca estandar. Estas funciones suelen estar optimizadas para realizar tareas comunes de forma eficiente.
  vii) gcc se comporta de cierta manera porque tiene que seguir estrictamente el lenguaje C, en mi opinion no va en contra de la especificación ya que el mismo lenguaje que sigue este compilador te permite lograr un código lo mas especifico posible.    
```
### Compilación Separada: Contratos y Módulos
```
c) Si se llega a agregar un argumento o sacar uno la funcion nos va tirar un error de compilación porque la funcion esta diseñada para recibir solo dos parámetros, por lo tanto si elimamos un argumento la funcion no va a poder cumplir lo que pide y si le agregamos va a tirar error porque no va a poder compilar por tener llena la pila

d)
  iv) La ventaja que nos da definir previamente el contrato y luego incluirlo tanto en el cliente y en el proveedor es que ya son bibliotecas que van a contar con las funciones de printf y prontf por lo tanto con solo incluirlas con el `#incluide` nos va permitir compilar el archivo sin tener que definir ninguna función previa 
```
