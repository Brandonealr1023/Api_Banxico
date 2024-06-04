# Api_Banxico
Uso de la API del SIE del Banco de México, replicando un grafico del informe trimestral del Banco de México, utilizando Matplotlib.

El objetivo de este repositorio es prectticar el uso de la API del Sistema de Información Económica del Banco de México y poder replicar 
un gráfico publicado en el Informe Trimestral Enero - Marzo del 2024.

La gráfica seleccionada para replicar fue la numero 103 del Informe, que se muestra a continuación.
![image](https://github.com/Brandonealr1023/Api_Banxico/assets/76232134/317d5ed3-11a2-442f-9c0c-553ba9fcffb0)

Las variables mostradas corresponden a:
* Objetivo para la tasa de interés interbancaria a 1 día.
* Inflación general
* Objetivo de Inflación del Banco de México del 3%

Lo destacado de este gráfico es mostrar la congruencia del banco central de seguir la tendencia de la inflación para tomar sus decisiones
de politica monetaria.

El proceso inicia con la recopilación de los indicadores.
Al entrar al sitio de la API del SIE esta es la página que encontramos.
![image](https://github.com/Brandonealr1023/Api_Banxico/assets/76232134/96311aaa-abbd-44ce-9399-0a155114370c)

La función que no interesa es GET series/:idSerie/datos, que como muestra  su descripción nos regresa la serie de tiempo de los indicadores
seleccionados para el periodo de tiempo disponible. 
![image](https://github.com/Brandonealr1023/Api_Banxico/assets/76232134/25a30c12-61c2-440a-82ae-d73f15a0aa22)

El siguiente paso es encontrar los indicadores necesarios en el apartado catálogo de series.
![image](https://github.com/Brandonealr1023/Api_Banxico/assets/76232134/43096ad3-7793-4381-91c4-550b8f485f22)

los ID de los indicadores son los siguientes.
	
	Índice Nacional de Precios al consumidor variación anual: SP30578
 TIIE de fondeo a 1 día Tasa de interés promedio mensual, en por ciento anual: SF331450

Finalmente se procesan los datos los datos con Pandas, y se gráfican utilizando Matplotlib buscando tener el mismo diseño que la gráfica original
obteniendo el siguiente resultado.
![image](https://github.com/Brandonealr1023/Api_Banxico/assets/76232134/fabf1658-2333-453c-87dc-17735b191684)


