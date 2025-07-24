# Unidad 1

## 🔎 Fase: Set + Seek

### Actividad 01

#### Ciclo feetch-decode-execute 
```
@1
D=A
@2
D=D+A
@16
M=D
@END
(END)
0;JMP
```
¿Qué crees que haga este programa?
Primero analice el codigo en el programa NAND2Tetris y mi primera hipotesis fue que era una suma y daba 3. Y en efecto era una suma que se guardó finalmente en la posición 16 de la memoria RAM y el programa se repite ciclicamente. Los cambios que observo en el contenido de la memoria y los registros es a medida que se les va pidiendo que se le almacene un dato nuevo.

```
@5
D=A
@10
D=D+A
@20
M=D
@END
(END)
0;JMP
```
Así quedó mi experimento y funciona de la misma forma que el código anterior, solo que esta vez se suma 5 y 10 y el resultado que es 15 se guarda en la posicioón 20 de la RAM.

#### ¿Qué diferencia hay entre los datos almancenados en la memoria ROM y en la RAM?
La diferencia es que en la memoria ROM está mi código el cual se va a ejecutar, entonces es como el que pone las reglas. En cambio, la RAM funciona como aquella que almacena los datos.

### Actividad 02

#### Explorando la arquitectura del computador Hack

Lo que puedo predecir de este código es que tiene algo que ver con las teclas, ya que tiene varias etiquetas a lo largo del código.

después de probar el código en efecto era sobre las teclas, pero adicional hay relación con la pantalla, donde cada que apretas una tecla, la pantalla se pinta full de negro

1) Identifica una instrucción que use la ALU y explica qué hace.
ALU (Arithmetic Logic Unit) se usa para comparar valores e incluso dirreciones y el que pude identificar seria D=D-A que se encarga de restar el valor en A del registro D usando ALU
2) ¿Para qué sirve el registro PC?
indica la dirección de la siguiente instrucción que se ejecutará, incluso incrementa cada ciclo
3) ¿Cuál es la diferencia entre @i y @READKEYBOARD?
@i  se refiere a una variable, que está en la RAM
@READKEYBOARD  se refiere a una etiqueta
4) Describe qué se necesita para leer el teclado y mostrar información en la pantalla.
Leer el teclado: leer el registro KBD, que es mapeo de memoria en RAM[24576]
Mostrar en pantalla: escribir en los registros de pantalla SCREEN (direcciones 16384–24575). Cada palabra representa 16 píxeles, donde 1 = píxel encendido
5) Identifica un bucle en el programa y explica su funcionamiento.
```
@READKEYBOARD
0;JMP
```
Se repite infinitamente, ya que 0;JMP siempre salta a (READKEYBOARD).
Esto permite que el programa revise el teclado y actualice la pantalla de forma continua.
6) Identifica una condición en el programa y explica su funcionamiento
```
@KBD
D=M
@KEYPRESSED
D;JNE
```
Permite distinguir entre dos comportamientos:
Si ninguna tecla está presionada → borra píxel (sube).
Si hay tecla presionada → dibuja nuevo píxel y baja.

### Actividad 03

#### Control de flujo con saltos
```
@5
D=M
@10
D=D-A
@MENOR
D;JLT
@7
M=0
@END
0;JMP
@7
M=1
@END
0;JMP
