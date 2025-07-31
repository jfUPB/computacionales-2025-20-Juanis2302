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


