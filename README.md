# RPA: Registro del Calendario de Facturación en el ERP Comercial

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

- Se coloca el mes de carga de calendario y el nivel de carga que es por sector.
![image](https://user-images.githubusercontent.com/31372472/140242798-2668e2ba-190a-47dc-9a9e-f9ae9614e8f8.png)

- Se muestra una nueva ventana donde debemos colocar el número de Sector al cual vamos a registrar su fechas del calendario.
![image](https://user-images.githubusercontent.com/31372472/140243061-cb474283-fa2e-447f-8d16-a728033e5c72.png)

- Se levanta una ventana pop up donde para el sector indicado se debe de colocar:
  * fecha de lectura que viene del excel.
  * fecha de facturación que viene del excel.
  * fecha de Reparto que viene del excel.

![image](https://user-images.githubusercontent.com/31372472/140243323-cccf234a-78bf-4c3d-ae02-92c26aac331b.png)

- Damos guardar y nos regresa a la pantalla inicial y debemos ir a la opción "Editar" en donde se nos levanta otra venta pop up.
- En esta ventana vamos a la opción "Editar Fecha de Vencimiento" y colocamos la fecha de vencimiento que se encuentra en el excel; y finalizamos guardando.
![image](https://user-images.githubusercontent.com/31372472/140243545-6e2dfffa-0b12-4640-a632-8c7cba8f4255.png)

El proceso descrito, líneas arriba, es para un sector y toma aproximadamente 1 minuto con 50 segundos; el calendario contiene la información de 55 sectores, es decir, si el proceso se da limpiamente este tomaría una 1 con 40 minutos.

La problemática no radíca en el registro de un sector, sino en el registro de todos los sectores, el cual en pleno proceso se vuelve tedioso y cansado para el usuario.

Equivocarse en el registro de un sector genera un impacto muy grande que perjudica a mas de 280 mil clientes y ni que decir de las perdidas financieras de la empresa.

La primera solución que se puede venir a la mente es una carga masiva del calendario, pero el problema es que el ERP es muy antiguo y el área de IT no tiene el personal adecuado para poder hacer la módificación.

Es por esta razón que se opta por la tecnología del RPA.

Nota: Para facilitar los conceptos vamos a indicar que un "sector" es una agrupación de clientes; y el total de clientes esta dividido en 55 sectores.

## Consideraciones de la solución:

- El programa utiliza el link del ERP que es de uso exclusivo de la organización para la cual laboro, pero si podrán visualizar el programa en python
- En el programa podrán observar que la solución esta configurada para la resolución de la computadora en la que la he desarrollado, por lo que si se ejecuta podría no coincidir con el tamaño de sus maquinas.
- Aquí un link del video de como funciona la solución: https://www.youtube.com/watch?v=OClEPz8TYfA&t=3s
