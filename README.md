# Data Quality Report-DQR (Spanish)


<p align="center">
  <img width="1200" height="400" src="https://github.com/EricPassosScience/DQR_Data_Quality_Report-Part_1/assets/97414922/3d7d5406-21f8-4c76-aab4-11a34b9a56ef">
</p>

***********************

## Consideraciones iniciales
Este trabajo se desarrolló en dos partes. La primera parte es el desarrollo del DQR mientras que la segunda se centrará en técnicas de detección de fraude en los mismos datos que usaremos para crear el DQR. Estás en la parte 1.

La parte más importante del trabajo está en el archivo python, donde se ubica todo el código y los resultados de los análisis. Sólo verás en este README una contextualización y algunos conceptos importantes. El código en el archivo Python y este README son complementarios, es decir, comprender uno depende de comprender el otro.

******************************

## ¿Qué es Data Quality Report?
El DQR es un informe analítico con el objetivo de comprender la organización de los datos, si son coherentes, si existen anomalías ampliamente visibles y resumir los datos (o al menos las variables más importantes) en función de la comprensión del problema empresarial.

En la práctica (en mi opinión), el DQR no es más que un análisis exploratorio muy bien documentado y realizado de la mano del equipo empresarial. En términos generales, el DQR contiene seis elementos: integridad, precisión, coherencia, uniformidad, integridad y actualidad.

*********************************

## Las grandes empresas utilizan Data Quality Report
Muchas de las empresas más grandes del mundo utilizan Data Quality Import como medida para asegurar que los datos de diferentes fuentes no solo sean recopilados, sino también refinados con precisión, evitando que el área de negocio tome decisiones equivocadas.

Un ejemplo de esto es UBER. Esta empresa desarrolló una herramienta llamada “Data Quality Monitor (DQM)”, que utiliza modelos estadísticos para identificar anomalías en los datos, alertando a los propietarios de las tablas de datos cuando se detectan problemas.

Según UBER, este enfoque era esencial para poder manejar de forma segura la gran cantidad de datos que ingresan a su sistema.
DQM analiza patrones de datos históricos y compara los datos actuales con las expectativas, lo que permite a los usuarios determinar si los datos siguen los estándares de calidad históricos.

Una vez que se encuentran anomalías, se recomienda a los usuarios que procedan con precaución en análisis posteriores.

Esta herramienta es una parte integral de la arquitectura del sistema de detección de anomalías de UBER. Y es muy similar a lo que encontrarás aquí, tanto en esta parte 1 como en la parte 2.
Aquí está la arquitectura simplificada de esta solución utilizada por UBER:

<p align="center">
  <img width="980" height="540" src="https://github.com/EricPassosScience/DQR_Data_Quality_Report-Part_1/assets/97414922/897119cc-5125-4367-82c7-054181a51f3e/imagem_2023-10-19_002240647.png">
</p>

REFERENCIA -> https://www.uber.com/en-BR/blog/monitoring-data-quality-at-scale/ 
********************************************

## DEFINICIÓN DEL PROBLEMA
Una compañía de seguros de propiedad en la ciudad de Nueva York en EUA, con el objetivo de calcular el valor del seguro de la mejor manera posible, nos contrató como científico de datos para analizar y detectar fraudes en los datos de transacciones inmobiliarias en toda la ciudad.

Sin embargo, primero la empresa necesita un informe que demuestre que los datos son fiables y actuales y que la calidad de la información que proporciona puede utilizarse para predecir posibles fraudes.

Destaco que aquí nos centraremos en DQR, la parte relacionada con la detección de fraude se hará en la parte 2 (próximamente).

*************************************************

## FUENTE DE DATOS
Para este proyecto (partes 1 y 2), utilizaremos datos reales disponibles públicamente. Se puede acceder a los datos en el portal de datos abiertos de la ciudad de Nueva York. Enlace -> https://data.cityofnewyork.us/Housing-Development/Property-Valuation-and-Assessment-Data/rgy2-tti8

<p align="center">
  <img width="1100" height="300" src="https://github.com/EricPassosScience/DQR_Data_Quality_Report-Part_1/assets/97414922/a0451d6b-03c5-43e3-a33b-09d26af2cd81/imagem_2023-10-20_220325472.png">
</p>

En el mismo enlace podemos encontrar el diccionario de datos que será fundamental para nuestro análisis.
********************************************
