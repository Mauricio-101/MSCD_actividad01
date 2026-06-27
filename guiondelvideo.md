# Guión de Presentación: Sistemas Expertos

## Diapositiva 1: Portada
"Buenos días a todos, profesor y compañeros. El día de hoy les presentaré el tema de **Sistemas Expertos**. Estos sistemas forman parte fundamental de la rama que conocemos como Inteligencia Artificial Simbólica. A lo largo de esta presentación, exploraremos cómo la inteligencia artificial logra capturar y aplicar el conocimiento humano especializado para resolver problemas del mundo real."

---

## Diapositivas 2 y 3: Introducción
"Para comenzar, debemos preguntarnos: **¿Por qué existen los Sistemas Expertos?** Nacen para resolver un problema muy concreto: el conocimiento de un experto humano es escaso, costoso y, a menudo, difícil de transferir. 

Como una rama de la Inteligencia Artificial, estos sistemas buscan resolver problemas complejos aplicando precisamente ese conocimiento especializado en un dominio específico. Su objetivo es reproducir el razonamiento y la toma de decisiones humanas, logrando que ese nivel de experiencia esté disponible en todo momento para el usuario. Hoy en día, aunque no siempre los veamos, operan silenciosamente detrás de diagnósticos médicos, filtros antifraude y sistemas de control industrial."

---

## Diapositivas 4 y 5: Definición
"Entonces, ¿qué es exactamente un Sistema Experto? Podemos definirlo como un **programa de cómputo diseñado para emular la capacidad de decisión de un experto humano dentro de un dominio acotado**. 

Lo hace combinando un conocimiento codificado con un mecanismo de razonamiento automático; en otras palabras, es la suma de una **Base de Conocimiento** y un **Motor de Inferencia**. A diferencia de muchos modelos actuales de aprendizaje automático que funcionan como 'cajas negras', un sistema experto aplica reglas lógicas de forma sistemática y trazable. No 'intuye', sino que sigue un proceso explícito, lo que le permite explicar siempre el porqué de cada conclusión."

---

## Diapositiva 6: Historia y Evolución
"Si revisamos su línea del tiempo, los sistemas expertos nacen en la Universidad de Stanford a mediados de los años 60, dentro de la corriente de la 'IA simbólica':

* **1965:** Destaca DENDRAL, considerado el primer sistema experto, el cual interpretaba espectros químicos. 
* **1976:** Surge MYCIN, un sistema con cerca de 600 reglas que diagnosticaba infecciones.
* **1980:** Aparece XCON, utilizado para configurar computadoras en la empresa DEC. 
* **Años 80:** Vivieron un fuerte auge comercial gracias a plataformas (shells) como EMYCIN y OPS5. 
* **1987:** Entraron en un periodo de declive, conocido como el 'invierno' de los sistemas expertos, provocado por su rigidez y altos costos de mantenimiento. 
* **2000s – Hoy:** Han evolucionado hacia sistemas híbridos, integrándose de manera exitosa con el Machine Learning."

---

## Diapositiva 7: Fundamentos (El concepto de conocimiento)
"Para entender cómo operan, debemos comprender cómo estructuran la información. En la base de la pirámide tenemos:

1. **Datos:** Son hechos aislados sin contexto (ej. el número '38.5 °C').
2. **Información:** Es el dato ya con contexto (ej. 'temperatura del paciente: 38.5 °C').
3. **Conocimiento:** Es la información interpretada con experiencia (ej. 'fiebre alta, posible infección').
4. **Sabiduría:** En la cima, es saber cuándo y cómo aplicar ese conocimiento en la práctica. 

El gran reto de estos sistemas es que codifican *conocimiento explícito*, ya que el *conocimiento tácito* (que incluye la intuición del experto) es el más difícil de capturar."

---

## Diapositivas 8 y 9: Componentes (Base de Conocimiento)
"Pasando a su arquitectura, el primer componente vital es la **Base de Conocimiento**. Aquí se almacenan los hechos, reglas y heurísticas del dominio, las cuales se extraen mediante ingeniería del conocimiento (entrevistas, observación, análisis documental). 

Este conocimiento puede representarse mediante reglas de producción, redes semánticas, árboles de decisión o marcos (frames). Su calidad determina directamente la calidad de las conclusiones del sistema. 

> **Ejemplo de regla de producción:**
> SI la temperatura es mayor a 38°C Y hay tos persistente, ENTONCES hay una posible infección respiratoria."

---

## Diapositiva 10: Componentes (Motor de Inferencia)
"El segundo gran componente es el **Motor de Inferencia**. Este es el elemento que 'razona', aplicando las reglas sobre los hechos disponibles para generar nuevas conclusiones. Funciona principalmente con dos métodos: 

* **Encadenamiento hacia adelante:** Parte de los hechos disponibles y deriva conclusiones paso a paso.
* **Encadenamiento hacia atrás:** Parte de una hipótesis y busca los hechos que la confirmen. 

Además, este motor incluye estrategias para resolver conflictos cuando múltiples reglas aplican al mismo tiempo."

---

## Diapositiva 11: Arquitectura Completa
"Viendo el panorama completo, la arquitectura fluye de la siguiente manera: el experto humano ayuda a construir la Base de Conocimiento, la cual interactúa directamente con el Motor de Inferencia. A su vez, el motor interactúa con el usuario a través de una Interfaz de Usuario, la cual cuenta con un Módulo de Explicación encargado de justificar el razonamiento seguido."

---

## Diapositiva 12: Funcionamiento (Paso a paso)
"El ciclo de funcionamiento se resume en cinco pasos: 

1. **Captura de datos:** El usuario aporta hechos sobre el problema a través de la interfaz.
2. **Comparación:** El motor cruza los hechos aportados con las reglas de la base de conocimiento.
3. **Activación de reglas:** Se disparan aquellas reglas cuyas condiciones se cumplen.
4. **Conclusión:** El sistema produce finalmente un diagnóstico o recomendación.
5. **Explicación:** Si el usuario lo solicita, el sistema justifica el razonamiento que siguió."

---

## Diapositivas 13 y 14: Clasificación
"Podemos clasificar los Sistemas Expertos en cuatro tipos principales: 

1. **Basados en reglas:** Usan la lógica SI-ENTONCES y son el enfoque más extendido por su simplicidad y facilidad de auditoría. (Ej. MYCIN, con ~600 reglas para diagnosticar infecciones bacterianas). La limitante es que el número de reglas crece rápido y genera conflictos.
2. **Basados en casos (CBR):** Resuelven problemas nuevos comparándolos con previos ya resueltos.
3. **De lógica difusa:** Manejan incertidumbre y términos imprecisos como 'alto' o 'poco'.
4. **Híbridos:** Combinan reglas con redes neuronales o algoritmos de aprendizaje automático."

---

## Diapositiva 15: Análisis (Ventajas y Desventajas)
"A nivel práctico, estos sistemas tienen **ventajas** innegables: ofrecen disponibilidad permanente sin fatiga, consistencia y trazabilidad en cada decisión tomada, democratizan un conocimiento experto que suele ser escaso, y aceleran enormemente la capacitación del personal nuevo. 

Sin embargo, sus **desventajas** son importantes: carecen por completo de sentido común fuera de su dominio específico, su construcción y mantenimiento son costosos (el famoso 'cuello de botella del conocimiento'), tienen dificultad para actualizarse ante cambios del dominio, y a diferencia del Machine Learning, no aprenden automáticamente de la experiencia."

---

## Diapositiva 16: Aplicaciones Actuales
"A pesar de esas limitaciones, sus aplicaciones hoy en día son críticas:

* **Medicina:** Apoyo al diagnóstico y recomendación de tratamientos (línea directa con MYCIN).
* **Finanzas:** Evaluación de riesgo crediticio, asesoría de inversión y detección de fraudes.
* **Industria:** Configuración de productos y mantenimiento predictivo.
* **Ciberseguridad:** Detección de intrusos (IDS) y aplicación de reglas de respuesta automatizada a incidentes."

---

## Diapositivas 17 y 18: Contexto en la IA y Conclusiones
"Para concluir, debemos situar a los Sistemas Expertos como el pilar fundamental de la Inteligencia Artificial Simbólica (conocimiento explícito y reglas), a diferencia de la IA moderna basada enteramente en datos (Machine Learning, LLMs). La IA actual no eliminó a los sistemas expertos; más bien, toma lo mejor de ellos, integrándolos en arquitecturas híbridas neuro-simbólicas para recuperar su gran fortaleza: la capacidad de explicación. 

Históricamente, demostraron que el conocimiento humano puede codificarse para automatizar decisiones confiables. Sentaron las bases conceptuales (reglas, inferencia, explicabilidad) que la IA sigue utilizando hoy en sectores críticos. Entender su funcionamiento y evolución es, por lo tanto, clave para comprender la historia y el futuro de la Inteligencia Artificial. 

Muchas gracias por su atención."


## LINK DEL VIDEO EN YOUTUBE:

https://youtu.be/J5wCC-_sA7I