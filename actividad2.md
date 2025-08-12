# EJEMPLO Calcular el area del triangulo #

Inicio

Leer base, altura

Calcular área = (base * altura) / 2

Mostrar área

Fin

# diagrama de flujo #
<img width="409" height="770" alt="diagrama" src="https://github.com/user-attachments/assets/0e9351cc-17ad-467c-a485-5e85174beb40" />

# EJERCICIO 2 #

Construye un algoritmo que, al recibir como datos el ID del empleado y los seis primeros sueldos del año, calcule el ingreso total semestral y el promedio mensual, e imprima el ID del empleado, el ingreso total y el promedio mensual.

## Solucion ##
```
Inicio
Leer ID, S1, S2, S3, S4, S5, S6
Total =S1 + S2 + S3 + S4 + S5 + S6
Promedio= Total/6
Escribir ID, Total, Promedio
Fin
```

### Diagrama de flujo 

<img width="249" height="527" alt="Ejercicio2 drawio" src="https://github.com/user-attachments/assets/fcd028fc-25ed-4d41-b33f-296f0d4f97c4" />



##TAREA##

Curso se evaluan con 7 notas 
conoce 6 notasd -> 70%
Calcular cuanto debe de sabar en la evaluacion final para aprobar con 3.0


#SOLUCION# 

```
Inicio
Leer N1, N2, N3, N4, N5, N6.
Promedio= N1+N2+N3+N4+N5+N6 / 6
Total= ((Promedio * 0.7) - 3.0 )/0.3
Escribir Nota minima para aprobar
Fin
```

#### DIAGRAMA DE FLUJO

<img width="311" height="591" alt="Tarea 2 drawio" src="https://github.com/user-attachments/assets/0e24c454-d03a-496d-b22f-f11f981f1216" />




##Ejercicios 3
Realice un algoritmo para determinar cuánto se debe pagar por equis cantidad de lápices considerando que si son 1000 o más el costo es de $85 cada uno; de lo contrario, el precio es de $90. Represéntelo con el pseudocódigo y el diagrama de flujo.


|Variables|Tipo|comentario|
|---------|----|----------|
|Lapices| Entrada|Cantidad de lapices|
|Precio | Salida|Precio total de los lapices|
|Valor unidad| Intermedia| Valor unitario cada lapiz |
|85, 90 | Constantes| No Cambian|

## Pseudocodigo

```
Inicio
Leer 
Sí lapices >=1000:
    valor_Unidad =85
sino 
    valor_Unidad =90
fin si
Precio = Lapices * valor_unidad
Escribir "El valor total es:",
Fin
```

### Diagrama de flujo

<img width="601" height="702" alt="Diagrama sin título drawio" src="https://github.com/user-attachments/assets/3eef864d-7dc8-405a-8112-d602c2598dba" />

### Ejercicio 4

Un almacén de ropa tiene una promoción: por compras superiores a $250 000 se les aplicará un descuento de 15%, de caso contrario, sólo se aplicará un 8% de descuento. Realice un algoritmo para determinar el precio final que debe pagar una persona por comprar en dicho almacén y de cuánto es el descuento que obtendrá. Represéntelo mediante el pseudocódigo y el diagrama de flujo.

### Analisis

|Variables | Tipo | Comentario |
|----------|------|------------|
|Total_compra | Entrada | Valor de la compra |
|Descuento | Salida | Descuento segun el valor de la compra |
|Precio_final | Salida | Valor a pagar |
|15%, 8%, $250000 | Constantes | Descuentos y valor limite |

### Pseudocodigo

```
Inicio
Leer total_compra
Sí total_compra > 250000:
    Descuento = Total_compra * 0.15
Si no
    Descuento = Total_compra * 0.8
Fin si
Precio_final= Total_compra - descuento
Escribir "Valor a pagar:", precio_final
Fin
```

### DIAGRAMA DE FLUJO



### Ejercicio 5
El director de una escuela está organizando un viaje de estudios, y requiere determinar cuánto debe cobrar a cada alumno y cuánto debe pagar a la compañía de viajes por el servicio. La forma de cobrar es la siguiente: si son 100 alumnos o más, el costo por cada alumno es de $65.00; de 50 a 99 alumnos, el costo es de $70.00, de 30 a 49, de $95.00, y si son menos de 30, el costo de la renta del autobús es de $4000.00, sin importar el número de alumnos.

### Analisis
|Variables|tipo| Comentario |
|---------|----|------------|
|Alumnos | Entrada | cantidad total de alumnos |
|costo_alumno | Salida | Costo segun la cantidad de alumnos |
|costo_total | Salida | Costo total a pagar |
|100, 50-99, 30-49, | Constantes| cantida de alumnos |

### Pseudocodigo
 ```
Inicio
Leer alumnos
Sí alumnos>=100
  Costo_alumnos=65
si no
  Si alumnos >=50
     costo_alumnos=70
  si no
      si costo_alumno>=30
         costo_alumnos=95
      si no
         costo_total=4000
         costo_alumnos=costo_total/alumnos
Fin si
costo_total=costo_alumnos * alumnos
Escribir costo_total, costo_alumno
Fin
```

<img width="811" height="902" alt="Diagrama sin título drawio" src="https://github.com/user-attachments/assets/a80a289f-d8b0-4743-936e-d70e9bd27685" />

      
###Tarea

  crear un pseudocódigo y diagrama de flujo con los siguientes pasos:
Ingresar día, mes, año de nacimiento. (Tres variables de entrada). 
Ingresar día, mes, año, actual (tres variables de entrada). 
Calcular edad.

|Variables| Tipo| Comentario|
|---------|-----|-----------|
|Dia de nacimiento|Entrada|Dia en el que nacio|
|Mes de nacimiento|Entrada|# mes en que nacio|
|Año de nacimiento|Entrada|Año en que nacio|
|Dia actual|Entrada|Dia actual|
|Mes actual|Entrada|#Mes actual|
|Año actual|Entrada|Año actual|
|Edad|Salida|Edad que tiene|

###Pseudocodigo

```
Inicio
Leer Dia de nacimiento, Mes de nacimiento, Año de nacimiento, Dia actual, Mes actual, Año actual
Si Mes de nacimiento < Mes actual
    Fin si
    Edad = Año actual - Año de nacimiento
Si no 
    Si mes de nacimiento > mes actual
        Fin si
        Edad = (Año actual - año de nacimiento) - 1
    Si no
        mes de nacimiento = mes actual    
            Si Dia de nacimiento <= Dia actual 
                Fin si 
                Edad = Año actual - Año de nacimiento 
            Si no 
                Edad = (Año actual - año de nacimiento) - 1
        
Escribir "Tu edad es"; Edad
Fin
```

### Diagrama de flujo 
<img width="778" height="1082" alt="image" src="https://github.com/user-attachments/assets/25f75fce-4b2a-4c73-987c-4d10343eaad9" />


