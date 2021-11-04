# Python RPA Business Case: Registro del Calendario de Facturación al ERP Comercial

## Requisitos:

- Instalación de librería TagUI: pip install tagui
- Instalación de librería Pandas: pip install pandas
- Conocmientos de Python

## Business Case:

Cada fin de mes se debe de registrar el calendario de facturación, que se encuentra en un archivo excel, a un módulo del ERP comercial, el proceso no es complicado y se de la siguiente manera:
- Se ingresa al módulo "Administración de Calendario".
- Se coloca el mes de carga de calendario
- Se indica el nivel de registros a cargar, que es por Sector.
- Se muestra una nueva ventana donde debemos colocar el número de Sector al cual vamos a registrar su fechas del calendario.
- Se levanta una ventana pop up donde para el sector indicado se debe de colocar:
  * fecha de lectura que viene del excel.
  * fecha de facturación que viene del excel.
  * fecha de Reparto que viene del excel.
- Damos guardar y nos regresa a la pantalla inicial y debemos ir a la opción "Editar" en donde se nos levanta otra venta pop up.
- En esta ventana vamos a la opción "Editar Fecha de Vencimiento" y colocamos la fecha de vencimiento que se encuentra en el excel; y finalizamos guardando

Este proceso para un sector toma aproximadamente un minuto con 50 segundos; el excel que contiene el calendario contiene la información de 55 sectores, es decir, si el proceso se da limpiamente este tomaría una hora con cuarenta minutos.

Nota: Para facilitar los conceptos vamos a indicar que un "sector" es una agrupación de clientes; y el total de clientes esta dividido en 55 sectores.
