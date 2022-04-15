
**Índice**
1. [Cleaning and manipulating text](##cleaning-and-manipulating-text)
2. [Working with numbers and dates](##working-with-numbers-and-dates)
3. [Defined Names for working more effectively with data](##defined-names-for-working-more-effectively-with-data)
4. [Tables for automating data manipulation](##tables-for-automating-data-manipulation)


## 1. Cleaning and manipulating text
| Funciones Excel | Comentario adicional |
| ------- | ----------- |
| CONCAT | 1. Concatenate desaparece. 2. Util cuando las columnas estan cerca puedas seleccionar y arrastrar por todas las celdas que quieres unir |
|Operador & | Puedes concatenar con este operador. Ejem. A2&"-"&B2. Puede ser utilizado pero no recomendado|
| UNIRCADENAS | Te permite ordenar más la unión de cadenas. Considerar que al igual que CONCAT, Es posible marcar todas las celdas por rango y el caracter inicial como separador|
|LIMPIAR|Limpia los 33 primeros del ASCII, que no son mostrados en pantalla. Uso común si la información proviene de otro sistema de archivos.|
|ESPACIOS|Comentario Adicional que borra izquierda y derecha y el segundo o mas espacios entre dos textos de la misma celda|
|NOMPROPIO|Primer caracter de cada palabra dentro de la celda es reemplazada por mayúscula|

(*) Adicionales para revisar son: UNICODE y UNICHAR. Como parte de funciones de limpieza de datos
## 2. Working with numbers and dates
### 2.1 Converting Data with VALUE and TEXT

| Funciones Excel | Comentario adicional |
| ------- | ----------- |
| VALOR | Conversión de texto a número, tener cuidado con manejo de errores |
| TEXTO | Depende del formato de fecha para la conversión |


> NOTA:
>> - Recomendable no formatear manualmente, sino, mediante formulas para orientar la limpieza hacia la automatización.   

>> - Tener considerado primero limpiar caracteres - 1. Cleaning and Manipulate - para evitar problemas de formateo en este punto   

### 2.2 Understanding dates and basic date functions

> NOTA:
>> - Las fechas en excel son realmente un número que se formatea como fecha. Al revisar las funciones DIA, MES Y AÑO se observa que el parametro es un número.

### 2.3 Generating Valid Dates using the DATE function

> NOTA:
>> - A la funcion: MES, es posible agregar 1&Celda para que pueda ayudar a la identificación del mes, en caso que este sea texto. Considerar que espera un número, sin embargo, el algoritmo de la función intenta buscar conversiones al parametro de entrada.
### 2.4 Calculations with Dates and using DAYS, NETWORKDAYS and WORKDAY
| Funciones Excel | Comentario adicional |
| ------- | ----------- |
| DIA.LAB.INT | En parametros de entrada, luego de fecha de inicio, dias a adicionar viene dias laborables, es posible colocar entre comillas los dias que se declaran como laborables. Ejm. "0000011", donde: 0: Dia laborable y 1: No laborable. Consideración adicional inicia en Lunes. Finalamente el parametro final te permite colocar una lista de feriados para que no sean incluidos. |
| DIAS.LAB.INT | La misma definición que la fórmula anterior solo que entre dos rangos de dias. |
   
> NOTA:
>> - .INT, Representa "Internacional", es decir permite habilitar mas opciones para que pueda soportar el contexto de un país (abre mas parametros en la función)

| Funciones Excel | Comentario adicional |
| ------- | ----------- |
| FIN.MES | Ultimo día de mes o de mes requerido |
| FECHA.MES | Retorna el mismo dia agregando el numero de meses ingresado por parametro |
   
> NOTA:
>> - =DIA.LAB.INTL(FIN.MES(D16,0)-1,1,"0000011",Holidays). En esta resta a FIN.MES y restando a dias laborables, es un artificio para que calcule incluyendo feriados
## Defined Names for working more effectively with data
### 3.1 s

## Tables for automating data manipulation
