<h1 align="center"> Simulación y Monitoreo de Variables Cardiovasculares y Hemodinámicas</h1>

El monitoreo de signos vitales constituye una herramienta fundamental en el área clínica y biomédica, ya que permite supervisar en tiempo real el estado fisiológico de un paciente mediante parámetros como frecuencia cardíaca, saturación periférica de oxígeno, presión arterial y temperatura. Estos sistemas de monitoreo son ampliamente utilizados en hospitales, unidades de cuidado intensivo y servicios de urgencias para apoyar el diagnóstico y la toma de decisiones médicas.

En esta práctica se realizó la evaluación funcional del monitor de signos vitales **uMEC 100** utilizando el simulador de parámetros hemodinámicos **Pronk OxSim OX-1**, el cual permite generar señales fisiológicas controladas para verificar el desempeño del equipo sin necesidad de utilizar un paciente real. Durante el desarrollo de la práctica se analizaron diferentes condiciones simuladas, como bradicardia, taquicardia, hipoxia y baja perfusión, evaluando la precisión de las mediciones, el comportamiento de las alarmas clínicas y la relación entre las señales visualizadas y los parámetros fisiológicos correspondientes.

## PARTE A - Revisión Bibliográfica

### Monitor de Signos vitales uMEC 100 
El monitor de signos vitales Mindray uMEC 100 es un equipo multiparámetro empleado para la supervisión clínica de variables fisiológicas como ECG, frecuencia cardíaca, SpO₂, presión arterial no invasiva, respiración y temperatura. Su función principal es apoyar el seguimiento continuo del estado del paciente mediante visualización en pantalla, alarmas clínicas y registro de parámetros, por lo que resulta fundamental en áreas como hospitalización, urgencias y cuidado crítico [1], [2].

<p align="center">
  <img src="https://github.com/user-attachments/assets/8f72a455-997d-4301-9054-e2edb7ad944d" width="500">
</p>

### Simulador Pronk OxSim OX-1 
El simulador Pronk OxSim OX-1 es un equipo portátil utilizado para verificar el funcionamiento de sistemas de pulsioximetría, ya que permite simular valores de saturación de oxígeno y frecuencia de pulso sin necesidad de conectarlo a un paciente real. Según la información técnica del fabricante, el OxSim OX-1 permite probar el sistema completo de SpO₂, incluyendo sensor, cable de extensión y monitor, con valores simulados de saturación y pulso definidos para pruebas biomédicas [3], [4].

<p align="center">
  <img src="https://github.com/user-attachments/assets/9cbe2d31-f131-4e55-9da3-ae1e8b0d0f79" width="500">
</p>

---

#### A.1 ¿Cómo colocar el uMEC100 en modo monitor?

Para configurar el uMEC100 en modo monitor se realizó el siguiente procedimiento:

<p align="center">
  <img src="https://github.com/user-attachments/assets/86ddd714-d779-433d-ae4a-9acd10270118"  width="500">
</p>

Este modo permite visualizar continuamente parámetros fisiológicos del paciente y activar alarmas clínicas configurables.

---

#### A.2 Parámetros fisiológicos simulables con el Pronk OxSim OX-1

El simulador Pronk OxSim OX-1 permite generar señales fisiológicas simuladas relacionadas principalmente con la pulsioximetría y la frecuencia cardíaca, utilizadas para verificar el correcto funcionamiento de monitores de signos vitales [3].

- **Saturación de oxígeno (SpO₂):** Simula diferentes porcentajes de saturación arterial de oxígeno, generalmente entre valores fisiológicos normales y estados de hipoxemia. Este parámetro representa el porcentaje de hemoglobina oxigenada presente en la sangre arterial y es medido mediante tecnología óptica basada en absorción de luz roja e infrarroja [4].

- **Frecuencia de pulso o frecuencia cardíaca:** El equipo puede generar pulsaciones simuladas expresadas en pulsos por minuto (bpm), permitiendo verificar la capacidad del monitor para detectar correctamente el ritmo cardíaco del paciente [3].

- **Índice de perfusión (dependiendo de la configuración):** Algunos modos de simulación permiten variar la intensidad de la señal pulsátil, simulando condiciones de perfusión baja o alta. Este parámetro representa la relación entre el flujo sanguíneo pulsátil y el flujo no pulsátil detectado por el sensor SpO₂ [5].

- **Condiciones de falla o interferencia:** El simulador puede generar escenarios de señal débil, ausencia de pulso o interferencias para evaluar la respuesta del monitor y sus alarmas clínicas [3].

<div align="center">

| Parámetro | Descripción |
|---|---|
| Frecuencia cardíaca (HR) | Simulación de latidos cardíacos en bpm |
| Saturación de oxígeno (SpO₂) | Simulación de niveles de oxigenación periférica |
| Baja perfusión | Simulación de señales débiles de flujo sanguíneo |
| Amplitud pulsátil | Modificación de intensidad de señal PPG |
| Arritmias simuladas | Alteraciones en frecuencia y periodicidad |

</div>

El simulador OxSim genera señales ópticas equivalentes a las producidas por tejido humano vascularizado. Esto permite evaluar el desempeño del monitor sin necesidad de utilizar pacientes reales.

---

#### A.3 Errores Máximos Permitidos (EMP)

En equipos de monitoreo clínico, los errores máximos permitidos (EMP) se encuentran definidos por normas internacionales y especificaciones de fabricantes biomédicos [6].

<div align="center">
   
| Parámetro | Error Máximo Permitido |
|---|---|
| Frecuencia cardíaca | ±3 bpm |
| Saturación SpO₂ | ±2 % |
| Tiempo de activación de alarmas | ≤ 10 s |

</div>



## Parte B — Desarrollo Experimental

### B.1 Tabla de Verificación de Alarmas

<div align="center">
   
| Límite Configurado | Valor Simulado | Alarma Activa | Tiempo de Respuesta |
|---|---|---|---|
| SpO₂ baja = 90% | 85% | Sí | 5 s |
| SpO₂ alta = 97% | 99% | Sí | 5 s |
| FC alta = 120 bpm | 140 bpm | Sí | 4 s |

</div>


### B.2 Simulación de Bradicardia

Se simula el FC en 40 bpm y el SpO₂ en 95% como se muestra en la imagen a continuación:

<p align="center">
  <img src="https://github.com/user-attachments/assets/d7abe0a5-a31c-42cd-bb0e-b10ee008ca1d"  width="500">
</p>

Los valores que se obtuvieron en uMEC100 se registraron en la siguiente tabla.

<div align="center">
   
| Parámetro | Simulado | Medido | Error Absoluto | Error % |
|---|---|---|---|---|
| FC | 40 bpm | 40 bpm | 0 bpm | 0% |
| SpO₂ | 95% | 96% | 1 | 1.05% |

</div>

El análisis de la tabla muestra que el monitor presentó una medición precisa para la frecuencia cardíaca (FC), ya que el valor medido coincidió exactamente con el valor simulado por el equipo de prueba, obteniéndose un error absoluto de 0 bpm y un error relativo del 0 %. En el caso de la saturación de oxígeno (SpO₂), se observó una diferencia mínima de 1 % entre el valor simulado y el medido, correspondiente a un error porcentual de 1.05 %, el cual se encuentra dentro de los límites de tolerancia aceptados para equipos de monitoreo clínico. En general, los resultados indican un funcionamiento adecuado del monitor de signos vitales y una correcta respuesta frente a las señales generadas por el simulador.

Tambien se establecio el limite de la alarma de SpO₂ inferior al 90%, como se observa en la siguiente imagen.

<p align="center">
  <img src="https://github.com/user-attachments/assets/c073ee00-287a-4834-99b0-502fc1708c4d"  width="500">
</p>

---

### B.3 Simulación de Hipoxia

Se simula el FC en 80 bpm y el SpO₂ en 85% como se muestra en la imagen a continuación:

<p align="center">
  <img src="https://github.com/user-attachments/assets/6ae8a504-d1b8-479e-8ee7-ee94f683bc3b"  width="500">
</p>

<div align="center">
   
| Parámetro | Simulado | Medido | Error Absoluto | Error % |
|---|---|---|---|---|
| FC | 80 bpm | 80 bpm | 0 bpm | 0% |
| SpO₂ | 85% | 85% | 0% | 0% |

</div>


El monitor de signos vitales presentó una respuesta completamente precisa frente a las señales generadas por el simulador. Tanto la frecuencia cardíaca (FC) como la saturación de oxígeno (SpO₂) coincidieron exactamente con los valores simulados, obteniéndose un error absoluto de 0 y un error porcentual del 0 % en ambos parámetros. Esto indica que el sistema de medición del monitor se encuentra funcionando correctamente y dentro de los márgenes clínicos aceptables para monitoreo biomédico.

Ademas se verifco y registro la activación de la alarma sonara/visual en el uMEC100.

<p align="center">
  <img src="https://github.com/user-attachments/assets/6383a68f-b009-4253-b455-8b087d3729e7"  width="500">
</p>

Durante la prueba se verificó el correcto funcionamiento del sistema de alarmas sonora y visual del Mindray uMEC 100. Al simular una condición fisiológica fuera de los límites establecidos, el equipo activó satisfactoriamente las alertas correspondientes, evidenciando una adecuada detección de eventos críticos y confirmando la capacidad del monitor para advertir oportunamente al personal clínico ante posibles alteraciones en los signos vitales del paciente.

---

### B.4 Simulación de Baja Perfusión

Se simula el FC en 80 bpm y el SpO₂ en 99% como se muestra en la imagen a continuación:

<p align="center">
  <img src="https://github.com/user-attachments/assets/b8cfb193-c887-4f0d-85a3-c6827f74abb3"  width="500">
</p>

<div align="center">
   
| Parámetro | Simulado | Medido | Error Absoluto | Error % |
|---|---|---|---|---|
| SpO₂ | 99% | 100% | 1% | 1.01% |

</div>

En la prueba adicional de saturación de oxígeno (SpO₂), el valor simulado fue de 99 % y el monitor registró un valor de 100 %, obteniéndose un error absoluto de 1 % y un error porcentual aproximado de 1.01 %. Este resultado demuestra que el equipo mantiene una alta precisión en la medición de SpO₂, ya que la diferencia observada es mínima y se encuentra dentro de los límites de tolerancia aceptados para equipos de monitoreo clínico. Ademas se verifco y registro la activación de la alarma sonara/visual en el uMEC100.

<p align="center">
  <img src="https://github.com/user-attachments/assets/18866e2d-d1a4-4e5e-a306-2027bf4e7e35"  width="500">
</p>

Al generar una señal fisiológica que sobrepasaba los rangos configurados en el monitor, el equipo respondió correctamente activando las alarmas visuales y sonoras programadas para advertir una condición anormal. La señal fotopletismográfica presentó distorsión y disminución en amplitud debido a la simulación de baja perfusión.

---

### B.5 Simulación de Taquicardia

Se simula el FC en 140 bpm y el SpO₂ en 95% como se muestra en la imagen a continuación:
<p align="center">
  <img src="https://github.com/user-attachments/assets/4a0b9257-d5a5-4f26-8384-f4d0f320319c"  width="500">
</p>

<div align="center">
   
| Parámetro | Simulado | Medido | Error Absoluto | Error % |
|---|---|---|---|---|
| FC | 140 bpm | 140 bpm | 0 bpm | 0% |
| SpO₂ | 95% | 98% | 3 | 3.16% |

</div>

La tabla muestra que la frecuencia cardíaca (FC) presentó una coincidencia exacta entre el valor simulado y el valor medido, obteniéndose un error absoluto de 0 bpm y un error porcentual de 0 %, lo que evidencia una respuesta precisa del monitor para este parámetro. En el caso de la saturación de oxígeno (SpO₂), el valor medido fue de 98 % mientras que el valor simulado fue de 95 %, generando un error absoluto de 3 % y un error porcentual aproximado de 3.16 %. Aunque existe una pequeña variación en la medición de SpO₂, el monitor continúa mostrando un comportamiento aceptable para aplicaciones clínicas y mantiene una adecuada capacidad de detección y monitoreo de los signos vitales simulados.
Adicionalmente se verifco y registro la activación de la alarma sonara/visual en el uMEC100.

<p align="center">
  <img src="https://github.com/user-attachments/assets/b7009439-fbcc-4e8f-810b-38497f8b169b" width="500">
</p>

Durante la simulación de una condición de frecuencia cardíaca elevada, el Mindray uMEC 100 activó correctamente la alarma sonora y visual, indicando que el sistema de alertas del monitor funciona adecuadamente ante valores fisiológicos fuera de los límites establecidos. 



En la práctica fue posible verificar el correcto funcionamiento del monitor uMEC100 mediante la simulación de diferentes condiciones fisiológicas y patológicas utilizando el simulador Pronk OxSim OX-1.

El monitor respondió adecuadamente ante:
- Episodios de bradicardia
- Hipoxia
- Baja perfusión
- Taquicardia

Asimismo, las alarmas clínicas se activaron dentro de tiempos aceptables y los errores de medición permanecieron dentro de rangos permitidos clínicamente.



## Análisis de Resultados

### Análisis 1

Para evaluar estadísticamente las diferencias entre los valores suministrados por el simulador y los valores medidos por el monitor uMEC 100, se analizaron los errores absolutos y porcentuales obtenidos en las diferentes condiciones simuladas: bradicardia, hipoxia, baja perfusión y taquicardia.

En el caso de la **frecuencia cardíaca (FC)**, los valores medidos por el monitor coincidieron exactamente con los valores simulados en todas las pruebas realizadas. Para bradicardia se obtuvo 40 bpm simulados y 40 bpm medidos; en hipoxia, 80 bpm simulados y 80 bpm medidos; y en taquicardia, 140 bpm simulados y 140 bpm medidos. Por lo tanto, el error absoluto promedio para FC fue de **0 bpm** y el error porcentual promedio fue de **0 %**, lo cual indica una alta precisión del monitor para este parámetro.

En cuanto a la **saturación de oxígeno (SpO₂)**, se observaron pequeñas diferencias entre los valores simulados y los medidos. En bradicardia se presentó un error de **1 %**, en hipoxia el error fue de **0 %**, en baja perfusión fue de **1 %** y en taquicardia fue de **3 %**. El error absoluto promedio para SpO₂ fue de:

<p align="center">

$$
\frac{1+0+1+3}{4}=1.25\%
$$

</p>

Mientras que el error porcentual promedio fue:

<p align="center">

$$
\frac{1.05+0+1.01+3.16}{4}=1.31\%
$$

</p>

Esto indica que el monitor presentó una buena respuesta en la medición de SpO₂, aunque con una ligera variabilidad en algunas condiciones, especialmente durante la prueba de taquicardia, donde se obtuvo el mayor error porcentual con **3.16 %**.

En general, los resultados muestran que el uMEC 100 tuvo un comportamiento adecuado frente a las señales generadas por el simulador. La frecuencia cardíaca presentó una coincidencia total con el valor de referencia, mientras que la SpO₂ mostró diferencias pequeñas y aceptables para una prueba de verificación funcional. Por lo tanto, se puede concluir que el equipo respondió de forma estable y confiable ante las condiciones fisiológicas simuladas.

### Análisis 2

La forma de onda visualizada en el monitor **uMEC 100** corresponde principalmente a la señal pulsátil detectada por el sensor de oximetría. Esta señal representa los cambios en el volumen de sangre arterial que ocurren con cada latido cardíaco. Por esta razón, cada pico de la onda se relaciona directamente con un pulso generado por el corazón.

La **frecuencia cardíaca (FC)** se obtiene a partir del número de pulsos detectados por minuto. Cuando la frecuencia cardíaca aumenta, los picos de la onda aparecen más cercanos entre sí, ya que hay más latidos en menos tiempo. Por el contrario, cuando la frecuencia cardíaca disminuye, los picos se observan más separados, indicando una menor cantidad de latidos por minuto.

La **saturación periférica de oxígeno (SpO₂)** se relaciona con la absorción de luz roja e infrarroja medida por el sensor. El monitor calcula este valor a partir de la señal pulsátil arterial y muestra el porcentaje de hemoglobina oxigenada en la sangre. Una SpO₂ alta indica una adecuada oxigenación, mientras que una SpO₂ baja puede representar hipoxemia o disminución del oxígeno disponible en sangre.

En general, una forma de onda estable, periódica y bien definida indica una buena detección del pulso y una medición confiable de la frecuencia cardíaca y la SpO₂. En cambio, una onda irregular, débil o con ruido puede afectar la precisión de los valores mostrados por el monitor, especialmente en condiciones como baja perfusión, movimiento del sensor o mala colocación del dispositivo.



## Preguntas para la Discusión

### ¿Cuál es el principio de operación del Pronk OxSim OX-1 para simular una onda pulsátil?

El simulador **Pronk OxSim OX-1** funciona mediante un sistema electrónico y óptico capaz de generar señales pulsátiles similares a las producidas por el flujo sanguíneo arterial en un paciente real. El equipo controla la emisión de luz en diferentes longitudes de onda, reproduciendo variaciones periódicas equivalentes a los cambios de absorción óptica que detecta un sensor de pulsioximetría durante cada latido cardíaco.

De esta manera, el sensor SpO₂ del monitor interpreta las señales generadas por el simulador como si provinieran de tejido biológico real, permitiendo evaluar parámetros como frecuencia cardíaca y saturación periférica de oxígeno sin necesidad de conectar el monitor a un paciente. Gracias a esto, el OxSim OX-1 puede utilizarse para pruebas funcionales, mantenimiento y verificación de monitores de signos vitales.


### ¿Por qué la SpO₂ baja puede ser un falso positivo en una situación de mala perfusión?

En condiciones de baja perfusión periférica, el flujo sanguíneo que llega a las extremidades disminuye considerablemente, lo que provoca que la señal pulsátil detectada por el sensor de oximetría sea más débil y menos estable. Debido a esto, el monitor puede tener dificultades para diferenciar correctamente la señal arterial del ruido o de otras interferencias presentes durante la medición.

Como consecuencia, el equipo puede mostrar valores de saturación periférica de oxígeno (SpO₂) artificialmente bajos, aun cuando el paciente mantenga niveles normales de oxigenación. Por esta razón, una SpO₂ baja en situaciones de mala perfusión puede interpretarse como un falso positivo, ya que el error se origina por la calidad deficiente de la señal y no necesariamente por una condición real de hipoxia.


## Conclusiones

- El simulador **Pronk OxSim OX-1** permitió reproducir de manera confiable diferentes condiciones fisiológicas y hemodinámicas, como bradicardia, taquicardia, hipoxia y baja perfusión, facilitando la evaluación funcional del monitor de signos vitales en un entorno controlado y seguro.

- El monitor de signos vitales **uMEC 100** presentó un comportamiento adecuado frente a las señales generadas por el simulador, mostrando mediciones precisas de frecuencia cardíaca y saturación periférica de oxígeno en la mayoría de las pruebas realizadas.

- El sistema de alarmas sonoras y visuales del monitor respondió correctamente cuando los parámetros simulados superaron los límites fisiológicos establecidos, evidenciando un adecuado funcionamiento de los mecanismos de alerta clínica del equipo.

- La señal fotopletismográfica observada en el monitor permitió identificar variaciones relacionadas con los diferentes estados fisiológicos simulados, demostrando la relación existente entre la forma de onda, la perfusión periférica y la frecuencia cardíaca del paciente.

- Los errores absolutos y porcentuales obtenidos durante las pruebas se mantuvieron dentro de rangos clínicamente aceptables, lo que indica que el equipo posee una adecuada capacidad de medición y monitoreo para aplicaciones biomédicas y hospitalarias.



## Bibliografía
[1] Mindray, uMEC Series Patient Monitor Operator’s Manual. Shenzhen, China: Mindray Bio-Medical Electronics Co., Ltd.

[2] Mindray, uMEC Series Patient Monitor Service Manual. Shenzhen, China: Mindray Bio-Medical Electronics Co., Ltd.

[3] Pronk Technologies, OxSim OX-1 Operation Instructions / Operator’s Manual. Pronk Technologies Inc.

[4] Pronk Technologies, “OX-1 OxSim Review,” Pronk Technologies. Disponible en línea.
[5] L. Cromwell, F. J. Weibell y E. A. Pfeiffer, Biomedical Instrumentation and Measurements, 2nd ed. Upper Saddle River, NJ, USA: Prentice Hall, 1980.

[6] International Electrotechnical Commission, IEC 60601-2-49: Particular Requirements for the Safety of Multifunction Patient Monitoring Equipment, Geneva, Switzerland, IEC, 2018.




