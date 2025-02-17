# CASO:

El área de auditoría de la compañía se encuentra analizando información del comportamiento de las EPS a nivel nacional desde sus indicadores de
calidad/atención.
Como fuente primaria de información se ha decidido hacer uso de los datos proporcionados por el portal de datos abiertos del Ministerio de Salud en el siguiente enlace:

https://www.datos.gov.co/Salud-y-Protecci-n-Social/Clicsalud-Indicadores-de-calidad-EPS/vw9t-pugy/data_preview

# ARQUITECTURA

La arquitectura propuesta parte desde la fuente de datos que extrae los datos mediante la api de Socrata que es una api open source que permite extraer datos de bases de datos del gobierno, esta data esta en formato JSON y se manda a través de una transferencia HTTPS, esta data puede ser manipulada posteriormente de diversas maneras pero en esta ocasión se propone el uso de un tablero en Jupyter (Enlace en los anexos) que usando las librerías de pandas y la sodapy nos permiten realizar todo el proceso de transformación de los datos de una manera eficiente, luego ese script de python se ejecuta en Power BI para tener a nuestra disposición los datos ya transformado y listos para su análisis. 

![image](https://github.com/user-attachments/assets/6f8d8cf0-0411-4761-9439-8bba17c29ea1)

# INDICADORES DE GESTION PROPUESTOS

- La duración promedio en días para el agendamiento de citas y la autorización de cirugías: este indicador nos permite observar que tan grave es la situación de las EPS en nuestro país, ya que podemos analizar, por ejemplo, que cirugías tienen un mayor tiempo promedio de autorización o revisar por que las citas de medicina general pueden llegar a tardar tanto tiempo en ser agendadas. 
- La duración promedio en días durante los periodos comprendidos entre el año 2016 a 2022, que son los años en que se tiene información, con este indicador podemos observar que ha ocurrido a través de los años, si ha existido una mejora en los servicios que ofrecen las EPS o si por el contrario se ha visto un empeoramiento en los tiempo de agendamiento y autorizaciones. 
El tablero propuesto fue realizado en Power BI y es el siguiente:

# VISUALIZACIÓN DE DATOS

- En el dashboard se encuentran los diferentes filtros los cuales se pueden aplicar en el dashboard para una mejor visualización de los datos y un análisis más exhaustivo.
- Se encuentran dos gráficos de barras que nos permiten visualizar el primer indicador de gestión y que permite visualizar la problemática de la demora de agendamiento de citas y de autorizaciones de citas mediante intervalos de tiempo útiles para realizar nuestros análisis
- En la ultima zona se encuentra un gráfico de líneas que nos permite visualizar el segundo indicador de gestión que nos permite analizar cómo han ido cambiando los tiempos de atención en las EPS a través de los años 

