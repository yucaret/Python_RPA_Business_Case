# RPA: Registro del Calendario de Facturación al ERP Comercial

## Requisitos:

- Instalación de librería TagUI: pip install tagui
- Instalación de librería Pandas: pip install pandas
- Conocmientos de Python

## Business Case:

Cada fin de mes, dentro del área de facturación, se registra el calendario de facturación a un módulo del ERP comercial de la empresa, el calendario contiene las fechas de cobro de recibo de luz de los clientes y otras fechas de importancia.

El formato del calendario es el siguientes:

![image](https://user-images.githubusercontent.com/31372472/140241760-1e25e45c-cab7-43c5-a31b-411a841522a8.png)

El proceso no es complicado y se da de manera manual y se realiza de la siguiente manera:

- Se ingresa al módulo "Administración de Calendario".
![image](https://user-images.githubusercontent.com/31372472/140242532-11fa59da-147a-481e-a96a-fa1fc44f4d8d.png)

- Se coloca el mes de carga de calendario.
- Se indica el nivel de registros a cargar, que es por Sector.
- Se muestra una nueva ventana donde debemos colocar el número de Sector al cual vamos a registrar su fechas del calendario.
- Se levanta una ventana pop up donde para el sector indicado se debe de colocar:
  * fecha de lectura que viene del excel.
  * fecha de facturación que viene del excel.
  * fecha de Reparto que viene del excel.
- Damos guardar y nos regresa a la pantalla inicial y debemos ir a la opción "Editar" en donde se nos levanta otra venta pop up.
- En esta ventana vamos a la opción "Editar Fecha de Vencimiento" y colocamos la fecha de vencimiento que se encuentra en el excel; y finalizamos guardando.

El proceso descrito, líneas arriba, es para un sector y toma aproximadamente 1 minuto con 50 segundos; el calendario contiene la información de 55 sectores, es decir, si el proceso se da limpiamente este tomaría una 1 con 40 minutos.

La problemática no radíca en el registro de un sector, sino en el registro de todos los sectores, el cual en pleno proceso se vuelve tedioso y cansado para el usuario.

Equivocarse en el registro de un sector genera un impacto muy grande que perjudica a mas de 280 mil clientes y ni que decir de las perdidas financieras de la empresa.

La primera solución que se puede venir a la mente es una carga masiva del calendario, pero el problema es que el ERP es muy antiguo y el área de IT no tiene el personal adecuado para poder hacer la módificación.

Es por esta razón que se opta por la tecnología del RPA.

Nota: Para facilitar los conceptos vamos a indicar que un "sector" es una agrupación de clientes; y el total de clientes esta dividido en 55 sectores.
