# Simulación y Monitoreo de Variables Cardiovasculares y Hemodinámicas

<div align="center">

## Laboratorio 5 — Instrumentación Biomédica y Biosensores

**Universidad Militar Nueva Granada**  
Facultad de Ingeniería — Ingeniería Biomédica  

---



</div>

---

# Tabla de Contenido

1. Introducción  
2. Objetivos  
3. Marco Teórico  
4. Materiales y Equipos  
5. Desarrollo Experimental  
   - Parte A  
   - Parte B  
6. Resultados  
7. Análisis de Resultados  
8. Preguntas para la Discusión  
9. Conclusiones  
10. Bibliografía  

---

# 1. Introducción

En el contexto clínico moderno, los monitores de signos vitales representan herramientas fundamentales para la vigilancia continua del estado fisiológico de un paciente. Variables como la frecuencia cardíaca (HR) y la saturación periférica de oxígeno (SpO₂) permiten evaluar rápidamente condiciones hemodinámicas y respiratorias críticas.

Para garantizar la confiabilidad de estos equipos, se emplean simuladores biomédicos especializados capaces de recrear condiciones fisiológicas y patológicas controladas. En esta práctica se utilizó el simulador **Pronk OxSim OX-1** junto con el monitor de signos vitales **uMEC100**, con el objetivo de evaluar la respuesta del monitor ante diferentes condiciones simuladas de frecuencia cardíaca y saturación de oxígeno.

Adicionalmente, se analizaron los sistemas de alarmas clínicas y la precisión de medición del monitor, aspectos esenciales en la seguridad del paciente y en los procesos de validación de equipos biomédicos.

---

# 2. Objetivos

## Objetivo General

Operar el simulador Pronk OxSim OX-1 y el monitor de signos vitales uMEC100 para realizar pruebas funcionales de monitoreo hemodinámico.

## Objetivos Específicos

- Identificar los modos de operación del simulador Pronk OxSim.
- Verificar los límites de medición del monitor uMEC100.
- Evaluar el funcionamiento de alarmas fisiológicas.
- Analizar el comportamiento de señales fotopletismográficas.
- Calcular errores absolutos y porcentuales en las mediciones obtenidas.

---

# 3. Marco Teórico

## 3.1 Pulsioximetría

La pulsioximetría es una técnica no invasiva utilizada para medir la saturación periférica de oxígeno (SpO₂) en la sangre. Su funcionamiento se basa en la absorción diferencial de luz roja e infrarroja por parte de la hemoglobina oxigenada y desoxigenada.

## 3.2 Frecuencia Cardíaca

La frecuencia cardíaca corresponde al número de latidos del corazón por minuto (bpm). Es una variable fisiológica fundamental para evaluar el estado cardiovascular del paciente.

## 3.3 Fotopletismografía

La señal fotopletismográfica (PPG) es una representación óptica de las variaciones de volumen sanguíneo en los tejidos periféricos. Esta señal permite calcular tanto la frecuencia cardíaca como la SpO₂.

## 3.4 Alarmas Clínicas

Los monitores multiparámetro incorporan alarmas visuales y auditivas que se activan cuando una variable supera límites previamente establecidos. Estas alarmas permiten actuar oportunamente ante condiciones críticas del paciente.

---

# 4. Materiales y Equipos

| Equipo | Descripción |
|---|---|
| Monitor de signos vitales | uMEC100 (Mindray) |
| Simulador biomédico | Pronk OxSim OX-1 |
| Sensor de SpO₂ | Compatible con uMEC100 |
| Computador | Registro y documentación |
| Libreta de laboratorio | Anotaciones experimentales |

---

# 5. Desarrollo Experimental

# Parte A — Revisión Bibliográfica

---

## A.1 ¿Cómo colocar el uMEC100 en modo monitor?

Para configurar el uMEC100 en modo monitor se realizó el siguiente procedimiento:

1. Encender el monitor mediante el botón principal de alimentación.
2. Esperar el inicio completo del sistema operativo del equipo.
3. Acceder al menú principal.
4. Seleccionar la opción **Modo Monitor**.
5. Verificar la correcta conexión de sensores y módulos de medición.

Este modo permite visualizar continuamente parámetros fisiológicos del paciente y activar alarmas clínicas configurables.

---

## A.2 Parámetros fisiológicos simulables con el Pronk OxSim OX-1

| Parámetro | Descripción |
|---|---|
| Frecuencia cardíaca (HR) | Simulación de latidos cardíacos en bpm |
| Saturación de oxígeno (SpO₂) | Simulación de niveles de oxigenación periférica |
| Baja perfusión | Simulación de señales débiles de flujo sanguíneo |
| Amplitud pulsátil | Modificación de intensidad de señal PPG |
| Arritmias simuladas | Alteraciones en frecuencia y periodicidad |

### Explicación

El simulador OxSim genera señales ópticas equivalentes a las producidas por tejido humano vascularizado. Esto permite evaluar el desempeño del monitor sin necesidad de utilizar pacientes reales.

---

## A.3 Errores Máximos Permitidos (EMP)

| Parámetro | Error Máximo Permitido |
|---|---|
| Frecuencia cardíaca | ±3 bpm |
| Saturación SpO₂ | ±2 % |
| Tiempo de activación de alarmas | ≤ 10 s |

Estos valores pueden variar según normativas internacionales y especificaciones del fabricante.

---

# Parte B — Desarrollo Experimental

---

## B.1 Tabla de Verificación de Alarmas

| Límite Configurado | Valor Simulado | Alarma Activa | Tiempo de Respuesta |
|---|---|---|---|
| SpO₂ baja = 90% | 85% | Sí | 5 s |
| SpO₂ alta = 97% | 99% | Sí | 5 s |
| FC alta = 120 bpm | 140 bpm | Sí | 4 s |

---

## B.2 Simulación de Bradicardia

### Configuración
- FC simulada: 40 bpm
- SpO₂ simulada: 95%

### Valores medidos en uMEC100

| Parámetro | Simulado | Medido | Error Absoluto | Error % |
|---|---|---|---|---|
| FC | 40 bpm | 41 bpm | 1 bpm | 2.5% |
| SpO₂ | 95% | 95% | 0 | 0% |

### Observaciones

La señal fotopletismográfica presentó una onda estable y periódica correspondiente a una frecuencia cardíaca baja.

---

## B.3 Simulación de Hipoxia

### Configuración
- FC simulada: 80 bpm
- SpO₂ simulada: 85%

| Parámetro | Simulado | Medido | Error Absoluto | Error % |
|---|---|---|---|---|
| FC | 80 bpm | 81 bpm | 1 bpm | 1.25% |
| SpO₂ | 85% | 86% | 1% | 1.17% |

### Resultado

Se activó correctamente la alarma sonora y visual del monitor al superar el límite inferior configurado.

---

## B.4 Simulación de Alta Saturación y Baja Perfusión

### Configuración
- SpO₂ simulada: 99%
- Modo: Low Perfusion

| Parámetro | Simulado | Medido | Error Absoluto | Error % |
|---|---|---|---|---|
| SpO₂ | 99% | 98% | 1% | 1.01% |

### Observaciones

La señal fotopletismográfica presentó distorsión y disminución en amplitud debido a la simulación de baja perfusión.

---

## B.5 Simulación de Taquicardia

### Configuración
- FC simulada: 140 bpm
- SpO₂ simulada: 95%

| Parámetro | Simulado | Medido | Error Absoluto | Error % |
|---|---|---|---|---|
| FC | 140 bpm | 142 bpm | 2 bpm | 1.42% |
| SpO₂ | 95% | 95% | 0 | 0% |

### Resultado

La alarma de frecuencia cardíaca elevada se activó correctamente.

---

# 6. Resultados

Durante la práctica fue posible verificar el correcto funcionamiento del monitor uMEC100 mediante la simulación de diferentes condiciones fisiológicas y patológicas utilizando el simulador Pronk OxSim OX-1.

El monitor respondió adecuadamente ante:
- Episodios de bradicardia
- Hipoxia
- Baja perfusión
- Taquicardia

Asimismo, las alarmas clínicas se activaron dentro de tiempos aceptables y los errores de medición permanecieron dentro de rangos permitidos clínicamente.

---

# 7. Análisis de Resultados

## Análisis 1

Los errores absolutos y porcentuales obtenidos fueron bajos en todas las pruebas realizadas. Esto indica una adecuada precisión del monitor uMEC100 frente a señales simuladas controladas.

## Análisis 2

La forma de onda fotopletismográfica varió directamente con la frecuencia cardíaca y las condiciones de perfusión simuladas.

- En bradicardia, la señal presentó períodos más amplios.
- En taquicardia, la señal mostró mayor frecuencia.
- En baja perfusión, la amplitud disminuyó y la onda presentó distorsión.

Esto demuestra la relación directa entre la calidad de la señal PPG y el estado hemodinámico simulado.

---

# 8. Preguntas para la Discusión

## Pregunta 1
### ¿Cuál es el principio de operación del Pronk OxSim OX-1 para simular una onda pulsátil?

El OxSim OX-1 utiliza emisores ópticos controlados electrónicamente para reproducir variaciones periódicas equivalentes al flujo pulsátil sanguíneo. Estas señales son interpretadas por el sensor SpO₂ como si provinieran de un paciente real.

---

## Pregunta 2
### ¿Por qué la SpO₂ baja puede ser un falso positivo en una situación de mala perfusión?

En condiciones de baja perfusión existe una reducción significativa de flujo sanguíneo periférico, lo que disminuye la calidad de la señal óptica detectada por el sensor. Esto puede generar errores de lectura e interpretaciones incorrectas de saturación baja, aun cuando el paciente no presente hipoxia real.

---

# 9. Conclusiones

- El simulador Pronk OxSim OX-1 permitió recrear exitosamente diferentes condiciones cardiovasculares y hemodinámicas.
- El monitor uMEC100 presentó un desempeño adecuado frente a las señales simuladas.
- Las alarmas clínicas funcionaron correctamente ante condiciones críticas configuradas.
- La señal fotopletismográfica evidenció cambios importantes según el estado fisiológico simulado.
- Los errores de medición obtenidos estuvieron dentro de márgenes aceptables clínicamente.

---

# 10. Bibliografía

1. Instituto de Salud Pública de Chile (ISP). *Guía para la Clasificación de Dispositivos Médicos según Riesgo*. 2021.

2. INVIMA. *ABC de Dispositivos Médicos - Guía Reguladora*. Bogotá, Colombia.

3. Medical IT. *Metrología Biomédica - Pronk OxSim*. Disponible en:  
https://www.medicalitech.com/producto/ox-sim/

4. Mindray. *Manual de Usuario uMEC100*.

5. Pronk Technologies. *OX-1 OxSim Flex Pulse Oximeter Tester User Manual*.

---

# Evidencias Experimentales

## Fotografías

> Inserte aquí fotografías del montaje experimental, conexiones y monitor.

---

## Registro de Ondas

> Inserte aquí capturas de pantalla de las señales fotopletismográficas observadas.

---

<div align="center">

## Fin del Informe

Repositorio elaborado para la asignatura  
**Instrumentación Biomédica y Biosensores**

</div>
