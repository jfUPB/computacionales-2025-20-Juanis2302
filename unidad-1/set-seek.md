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
3) 


