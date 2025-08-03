# Unidad 2

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

