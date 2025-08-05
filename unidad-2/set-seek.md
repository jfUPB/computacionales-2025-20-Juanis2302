l # Unidad 2

## 🔎 Fase: Set + Seek

### Actividad 01
#### Dibujando un punto en la pantalla
<img width="720" height="357" alt="image" src="https://github.com/user-attachments/assets/19e4769a-5f59-4e21-8497-c96c95dfb56e" />
<img width="240" height="145" alt="image" src="https://github.com/user-attachments/assets/04e63bda-8ee7-40fa-a761-b005aae91215" />
Así quedo el primer punto, tanto probado en el programa como el codigo en notas 


### Actividad 02
#### Dibujando una linea horizontal
<img width="868" height="189" alt="image" src="https://github.com/user-attachments/assets/fe268e6e-db3f-4b06-9f79-b681d60171d4" />


### Actividad 03
#### Entrada salida interactiva
<img width="659" height="323" alt="image" src="https://github.com/user-attachments/assets/e340fb32-1a1b-4826-b51b-e144d317e5ee" />
<img width="490" height="624" alt="image" src="https://github.com/user-attachments/assets/35f70c9c-9a5f-4a16-a7fe-441703a127bb" />

Así ha quedado tanto en el programa como en notas, siguiendo y teniendo de apoyo las instrucciones del profesor


### Actividad 04
#### Convierte un ciclo while en un ciclo for
Este es el código, es el mismo. 
```
// Adds1+...+100.
 @i // i refers to some memory location.
 M=1 // i=1
 @sum // sum refers to some memory location.
 M=0 // sum=0
 (LOOP)
 @i
 D=M // D=i
 @100
 D=D-A // D=i-100
 @END
 D;JGT // If(i-100)>0 gotoEND
 @i
 D=M // D=i
 @sum
 M=D+M // sum=sum+i
 @i
 M=M+1 // i=i+1
 @LOOP
 0;JMP // GotoLOOP
 (END)
 @END
 0;JMP // Infinite loop
```
- Son equivalentes el for y el while, porque uno se convierte en el otro. Basicamente son iguales
<img width="890" height="578" alt="image" src="https://github.com/user-attachments/assets/823ec9bb-5a33-4126-ae84-87c19a839405" />
Así quedó en el simulador


### Actividad 05
#### Punteros
- Son variables y se guardan direcciones
  <img width="86" height="333" alt="image" src="https://github.com/user-attachments/assets/bc44a5d2-a03a-4e65-b4e7-37cb70220d1e" />
  

  
### Actividad 06
#### Experimenta con arreglos
Primero podría decir que este código lo que hace es sumar todos los elementos del arreglo
<img width="102" height="384" alt="image" src="https://github.com/user-attachments/assets/c531dd58-d722-4e9a-b5b4-5796b5a3502d" />
Yo lo haría así, como primer intento, lo empecé en la dirreción 16 porque así lo pedía el programa. A continuación realizaré mi paso a paso
<img width="348" height="609" alt="image" src="https://github.com/user-attachments/assets/e661e60a-8009-424a-98b7-9db6ddc46cab" />
Al final me quedó así, pero sigo teniendo dudas y sigo prefiriendo el inicio del primero
<img width="121" height="607" alt="image" src="https://github.com/user-attachments/assets/4ac8d81d-e79f-474f-859d-605f3375ca4e" />
entonces lo cambié y lo hice de nuevo y me quedó así 

### Actividad 07
#### Autoevaluación
1) En ensamblador Hack, un puntero no es más que un espacio de memoria que guarda la dirección de otro espacio
Para hacer algo parecido a p = &x, lo que hago es tomar la dirección de x y guardarla en una posición como @p
2) Para acceder a arr[j] en Hack, imagino que arr empieza en una posición fija (por ejemplo, la 20).
Luego, si j está en una variable, sumo esa posición base con j para obtener la dirección exacta

1) El concepto más difícil para mí fue el control de flujo,especialmente los if y los for. Los ciclos especialmente,muno solo escribe la condición y el cuerpo, pero en ensamblador hay que hacer saltos manuales, como decir: “si esto no se cumple aquí, sigue por allá”. Es un concepto que generalmente me cuesta mas entender y hacerle pruebas.
2) Ir probando paso por paso me permitió no perderme en lo que estaba haciendo. Además, al ver los valores en la RAM en cada paso, entendía mucho mejor qué estaba pasando por dentro. Sin ese enfoque, habría colapsado con tanta cosita
3) Ahora me siento muy segura al identificar cuándo en C++ se está usando un acceso a memoria indirecta, como *ptr o arr[i]. Adicional del proceso paso a paso que hace el profe ya entiendo que por debajo eso significa ir a una dirección específica de la memoria y eso se traduce en A=D+A, D=M, etc.
   
### Actividad 09
#### Feedback
La actividad que más me ayudó fue cuando nos tocó traducir ese for en C++ que sumaba los valores del arreglo… eso sí me hizo entender cómo se ve en bajo nivel algo que uno en C++ hace sin pensarlo. Literalmente, ver que arr[j] era una suma de dirección + índice fue como: "ahhh, así funciona de verdad".
También me ayudó muchísimo que todo estuviera dividido en pasos (predice, ejecuta, observa, reflexiona), porque así no me sentí tan perdida. Siento que sin eso me habría abrumado mucho más.

Dejar de hacer: Lo de tener que meter los valores del arreglo uno por uno, incluso dejar de hacer todo tan tecnico o tan estricto, hacer varias pruebas sirve pme pareció eterno. Entiendo que sirve para ver cómo se llena la memoria, pero llega un punto donde uno ya entendió la idea y se vuelve más una cosa mecánica.
Yo cambiaría eso por un archivo RAM que uno pueda cargar rápido y ya enfocarse en el código de verdad. A veces me afano mucho y termino pasando todos estoss temas por alto.

Empezar a hacer: Una idea que me habría ayudado es ver una animación o algo visual que muestre cómo cambia la memoria mientras se ejecuta el código. O sea, como ver un puntero moviéndose, o cómo cambia A, M, D... siento que eso me ayudaría a entender más fácil, porque todo en ensamblador es muy abstracto. 

Ritmo y dificultad: Fue un salto grande. Pasamos de hacer cosas básicas e incluso muy grandes a pensar en cómo funciona todo desde cero. A veces me costó y mucho, pero no sentí que fuera imposible, solo que necesitaba más paciencia de la que suelo tener me ayudó mucho ir paso a paso, probar cada cosa por separado y no correrme a hacer todo el programa de una. 

La verdad al principio sí me sentí insegura y que no iba a ser capaz, pensé que no iba a entender nada, pero cuando me puse en modo prueba y error, y me tomé el tiempo de verdad, me di cuenta de que sí soy capaz. Me ayudó mucho escribir las cosas a mi manera y buscar explicaciones que me sirvieran a mí, como con las pruebas o ejemplos tontos que me inventaba. Siento que en esta unidad empecé a pensar como programadora de verdad. No solo repito el código, sino entiendo verdaderamente lo que pasa por dentro.
Gracias por hacer un curso que de verdad se siente pensado para que uno aprenda, y no solo para pasar.

