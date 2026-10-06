# TP1 – Metodología de la Investigación (UNTREF, Ingeniería de Sonido)

**Artículo analizado:** Scherer, R. C., Shinwari, D., De Witt, K. J., Zhang, C., Kucinschi, B. R. y Afjeh, A. A. (2002). *Intraglottal pressure distributions for a symmetric and oblique glottis with a uniform duct (L)*. J. Acoust. Soc. Am., 112(4), 1253–1256. DOI 10.1121/1.1504849.

> Nota: el artículo es una *carta al editor* de 4 páginas, por lo que muchos elementos (hipótesis, marco teórico, validez) no están explicitados y se infieren del texto. Cuando es una inferencia nuestra, se indica.

---

## 1. Planteamiento del problema cuantitativo

**(a) Objetivos.** El artículo no tiene una sección de objetivos, pero se deducen de la introducción:

- Medir la distribución de presión sobre las paredes de una glotis de conducto uniforme (diámetro mínimo 0,04 cm, ángulo incluido 0°) para dos configuraciones: simétrica (oblicuidad 0°) y oblicua (20°).
- Determinar si la oblicuidad genera presiones desiguales entre ambos lados de la glotis (convergente vs. divergente), como ya se había visto con una glotis divergente de 10° y oblicuidad de 15° (Scherer et al., 2001).
- Interpretar esas diferencias con simulación CFD (FLUENT).

Están expresados con claridad razonable (el resumen es preciso), pero de forma implícita y sin enunciado formal; "deducir cómo la oblicuidad afecta las fuerzas sobre las cuerdas vocales" es algo más vago que lo medido, que son presiones de pared.

**(b) Preguntas.** Implícitas: ¿son iguales las presiones en ambos lados en la glotis simétrica? ¿Difieren en la oblicua, y en qué región y en qué magnitud (% de la presión transglótica)? ¿Cómo se comparan simétrica y oblicua? ¿Qué mecanismo físico explica las diferencias? Son congruentes con los objetivos: cada pregunta se responde en un apartado de Resultados (III.A, III.B, III.C, III.D). La relación con la fonación (fases fuera de sincronía entre los pliegues) queda como pregunta abierta en la Discusión.

**(c) Justificación.** La oblicuidad glótica aparece en fonación normal y patológica (por diferencias de fase entre pliegues). Las fuerzas intraglóticas pueden diferir de las de la glotis simétrica de igual ángulo, y podrían influir en el movimiento fuera de fase de los pliegues. Aporta datos empíricos para validar modelos numéricos y físicos de la fonación, y es continuación de una línea de investigación (segundo trabajo de la serie). Financiado por NIH (DC03577), lo que indica relevancia para trastornos de la comunicación.

**(d) Viabilidad.** Fue viable: modelo de acrílico a escala 7,5:1, 14 tomas de presión, flujo constante, medición de caudal y presión, y software CFD comercial. Conviene señalar que ya contaban con el modelo y el método del estudio previo, y que los pliegues vocales eran insertos intercambiables, lo que redujo costos. Limitaciones prácticas: las tomas están sólo en un lado, por lo que requirió dos juegos de pliegues para medir "ambos lados".

**(e) Ética.** No intervienen personas ni animales: es un modelo físico y simulación, por lo que no plantea problemas éticos relevantes ni requiere consentimiento informado. Las consecuencias son beneficiosas (mejor comprensión de la fonación y su patología). Se declara la fuente de financiamiento y se agradece a revisores.

---

## 2. Construcción del marco teórico

**Índice del marco teórico (inferido de Introducción, Métodos y Discusión):**

1. Fonación y oblicuidad glótica (normal y patológica): von Leden et al. (1960); Svec y Schutte (1996); Svec et al. (1999).
2. Antecedentes del grupo: Scherer et al. (2001), glotis divergente oblicua (10°/15°); diferencia del 27 % en la entrada.
3. Fuerzas de presión intraglótica sobre los pliegues vocales y su relación con el movimiento fuera de fase.
4. Dinámica de fluidos aplicada: ecuación de Bernoulli, separación de flujo por gradientes adversos de presión, asimetría del chorro supraglótico (Cherdron et al., 1978; Tsui y Wang, 1995), número de Reynolds.
5. Modelado físico (modelo M5 a escala 7,5:1) y modelado computacional (ecuaciones de Navier–Stokes, FLUENT).

**(a) ¿Completo?** Parcialmente. Es suficiente para una carta y está bien anclado en el estudio previo, pero es breve: pocas referencias, sin revisión de modelos de fonación (p. ej. teorías de vibración de pliegues) ni de otros estudios de presión intraglótica en glotis oblicuas. Depende mucho de trabajos propios.

**(b) ¿Relacionado con el problema?** Sí. Cada elemento se usa luego: la oblicuidad como variable motivada por la literatura clínica; Bernoulli para explicar el aumento del 18 % del diámetro en la toma 6; la asimetría del chorro para explicar las diferencias cerca de la salida.

**(c) ¿Ayudó a los investigadores?** Sí: (i) justificó la hipótesis de partida (que la oblicuidad genera presiones desiguales), (ii) guió el diseño (misma geometría y metodología que en el estudio previo, para poder comparar), (iii) dio herramientas de interpretación (Bernoulli, separación de flujo) y (iv) permitió contrastar los resultados con el trabajo anterior en la Discusión.

---

## 3. Definición del alcance de la investigación

**Alcance predominante: descriptivo**, con componente **correlacional/explicativo limitado** en la parte computacional y de **continuación exploratoria** respecto de la serie.

- **Etapa inicial (antecedentes y motivación):** *exploratorio* — la oblicuidad glótica era un fenómeno poco estudiado; el primer estudio (2001) lo exploró y éste lo continúa con una geometría distinta.
- **Etapa central (mediciones):** *descriptivo* — mide presiones en 14 tomas para 4 presiones transglóticas y 2 geometrías, y expresa diferencias como % de la presión transglótica.
- **Etapa final (CFD y discusión):** *explicativo (parcial)* — usa FLUENT y Bernoulli para dar razones de las diferencias (mayor diámetro efectivo, flujo incidente sobre el lado convergente, separación del flujo).

Respuestas a las cuestiones:

- **(a) ¿Vincula variables?** Parcialmente: relaciona oblicuidad con diferencia de presión entre lados y con posición axial, pero sin análisis correlacional formal (sin coeficientes).
- **(b) ¿Describe y mide?** Sí, es lo central: mide presión de pared y caudal, y define variables (presión relativa a la transglótica, distribución por toma).
- **(c) ¿Busca causas?** En parte: explica con CFD y Bernoulli por qué hay diferencias, pero no manipula causas de forma aislada más allá de la oblicuidad. Deja explícitamente abierto el vínculo con la fase entre pliegues.
- **(d) ¿Desarrolla métodos para estudios más profundos?** Sí: el procedimiento de invertir los pliegues y de conmutar el lado del flujo con una guía de papel para medir "ambos lados" es un método reutilizable, y el trabajo prepara estudios dinámicos posteriores.

---

## 4. Formulación de hipótesis

El artículo **no enuncia hipótesis formales**. Las hipótesis implícitas son:

- **H1 (de investigación, causal/diferencia de grupos):** La oblicuidad glótica (20°) produce presiones distintas en los lados convergente y divergente en la región de entrada de la glotis.
- **H0 (nula):** En la glotis simétrica las presiones son iguales en ambos lados (confirmada en los resultados: diferencias pequeñas, sólo cerca de la salida, 1,35 %–3,1 %).
- **H2 (descriptiva de un valor pronosticado):** el aumento del 18 % del diámetro en la toma 6 reduce la caída de presión un 28,2 % según Bernoulli (se verifica: dentro del 2,7 % en el lado divergente).
- **H3 (consistencia con el estudio previo):** el lado convergente recibe mayor presión que el divergente, como ya observado con la glotis divergente.

**(a) Redacción.** Al no estar explícitas, no están redactadas "formalmente"; son entendibles por el contexto, aunque el lector debe inferirlas.

**(b) Tipo.** H1: de investigación y causal/diferencia entre dos condiciones (lado convergente vs. divergente); H0: nula; H2: descriptiva de valor pronosticado.

**(c) Variables.**

- *Independientes:* oblicuidad (0° vs. 20°) y lado de la glotis (flujo/no-flujo; convergente/divergente); presión transglótica (3, 5, 10, 15 cm H₂O).
- *Dependientes:* presión de pared en cada toma (expresada como caída de presión desde la tráquea), diferencias transversales entre lados como % de la presión transglótica.
- *Definición operacional:* presión medida con tomas de 0,033 cm de diámetro interno en las paredes del modelo; caudal fijo por condición (80,8; 106,4; 161,7; 205,0 cm³/s, ±2 %). Conceptualmente, "oblicuidad" es la inclinación del eje glótico respecto del flujo traqueal axial.

**(d) Mejoras.** Enunciar hipótesis y criterios de decisión explícitos antes de medir; definir un umbral de diferencia significativa (p. ej. cuánto es "esencialmente igual"); formular una hipótesis sobre la relación con la fase de los pliegues, que hoy queda como mera especulación ("suggesting… may influence").

---

## 5. Elección del diseño de investigación

**Diseño: experimental (de laboratorio, modelo físico) con comparación de condiciones**, más un componente computacional. No es cuasi-experimento con personas; es manipulación directa de variables en un modelo. No hay componente no experimental relevante (salvo la simulación, que es complementaria).

**Diseño experimental**

- **(a) Variables independientes:** oblicuidad (0° / 20°), lado de la glotis (convergente/divergente, o flujo/no-flujo), presión transglótica (3, 5, 10, 15 cm H₂O) y posición axial (toma 1 a 16).
- **(b) Variables dependientes:** presión de pared (caída de presión respecto de la tráquea) en cada toma; diferencia entre lados (% de la presión transglótica); caudal (que resulta de la presión impuesta).
- **(c) Grupos:** no hay individuos. Las "unidades" son las configuraciones geométricas: pliegues simétricos; dos pares oblicuos (uno con tomas en el lado divergente y otro invertido con tomas en el lado convergente); y las dos direcciones de flujo supraglótico en el caso simétrico.
- **(d) ¿Se gradúa el estímulo?** Sí: cuatro niveles de presión transglótica (3, 5, 10, 15 cm H₂O) con caudal constante, que cubren bajo y alto número de Reynolds.
- **(e) Invalidación interna:**
  - *Instrumentación:* tomas sólo en un lado → se controla invirtiendo los pliegues y repitiendo; la comparación depende de la reproducibilidad entre dos pares de piezas (posible sesgo de fabricación; no se informa).
  - *Asimetría del flujo supraglótico:* el chorro se desvía hacia un lado → se controla (parcialmente) observando la dirección con una varilla con pelos y conmutando el lado con una guía de papel; aun así afecta las tomas ≥ 11.
  - *Diferencia de diámetro* (18 % mayor en la toma 6 oblicua vs. simétrica): variable de confusión reconocida y cuantificada con Bernoulli, no eliminada.
  - *Historia/maduración/mortalidad* no aplican.
- **(f) Invalidación externa:**
  - Modelo rígido, a escala 7,5:1, sin falsas cuerdas, sin movimiento de pliegues, flujo estacionario (no pulsátil), un solo diámetro mínimo (0,04 cm) y un solo ángulo de oblicuidad (20°), con aire de laboratorio y conducto rectangular. Se controla parcialmente por similitud geométrica y por trabajar en rangos de presión fisiológicos, pero la extrapolación a la glotis humana en vibración no está demostrada.

**Diseño no experimental:** no aplica al componente principal. La simulación CFD es un estudio descriptivo/explicativo transeccional (una condición, 5 cm H₂O, "las otras fueron similares").

---

## 6. Selección de la muestra

**(a) Muestra.** No hay muestra de sujetos. Las unidades son: el modelo M5 con tres pares de pliegues (uno simétrico y dos oblicuos), 14 tomas de presión en la superficie, 4 niveles de presión transglótica y dos direcciones de flujo. Fue elegida por diseño (geometría uniforme, 0,04 cm de diámetro mínimo, longitud de 1,2 cm, conducto de 0,3 cm en tamaño humano), no por muestreo probabilístico.

**(b) ¿Adecuada?** Es adecuada para un estudio de física del flujo en un modelo, donde la "muestra" es el conjunto de condiciones. Es limitada en la variedad de geometrías (una sola uniforme, un solo ángulo) y no se reportan repeticiones independientes, lo que restringe la estimación de la variabilidad.

**(c) Principales resultados.**

- Glotis simétrica: presiones esencialmente iguales en ambos lados; diferencias pequeñas aguas abajo (toma 11: 1,35 %; toma 15: 3,1 % de la presión transglótica a 15 cm H₂O).
- Glotis oblicua (20°): el lado convergente tiene mayor presión en la entrada: 21,4 % (DE 0,45 %) en la toma 6 y 16,1 % (DE 0,37 %) en la toma 7; en las tomas 8–10 las presiones son similares; en la toma 12 difieren sólo 1,7 %.
- Las presiones internas son mayores en el caso oblicuo hasta la toma 10 (diámetro 18 % mayor en la toma 6; reducción de caída de presión del 28,2 % prevista y verificada dentro del 2,7 %).
- CFD: mayor velocidad y menor presión en la pared divergente; separación del flujo en ambas paredes cerca de la salida, primero en la convergente.
- Esta oblicuidad crearía presiones aguas arriba que podrían influir en el movimiento fuera de fase de los pliegues.

**(d) ¿Generalizable?** Hacia otras condiciones de la misma familia (geometrías uniformes, flujo estacionario, otros caudales de ese rango), con cautela. Hacia glotis humanas reales, sólo de manera cualitativa.

**(e) ¿Son serias las generalizaciones?** Los autores son prudentes: usan "suggesting" y "may influence", y dejan abierta la relación con la fase y las perturbaciones de flujo. Las generalizaciones a la fonación real serían prematuras sin pruebas con pliegues móviles, flujo pulsátil y otras oblicuidades/geometrías.

---

## 7. Recolección de los datos cuantitativos

**(a) ¿Confiable?** Razonablemente. Las mediciones de caudal tienen una incertidumbre de ±2 %, y la repetibilidad de las diferencias entre lados es alta: desviaciones estándar de 0,45 % y 0,37 % (sobre las cuatro presiones transglóticas) para las diferencias del 21,4 % y 16,1 %; las diferencias en la toma 12 tienen DE 0,8 %. No se informa la incertidumbre del transductor de presión en esta carta (se remite al estudio previo).

**(b) Técnica de confiabilidad.** Repetición del experimento en cuatro condiciones de presión y consistencia entre ellas (media y desviación estándar); dos conjuntos empíricos por presión transglótica en el caso simétrico (lado de flujo y no-flujo); inversión de pliegues y de dirección del flujo. Los métodos de medición y las exactitudes se declaran "idénticos al estudio anterior" (Scherer et al., 2001).

**(c) Validez.** No hay una prueba formal en este trabajo. La validez se apoya en: (i) simetría observada en el caso simétrico, que actúa como control; (ii) concordancia con Bernoulli (28,2 % previsto vs. verificado dentro del 2,7 %); (iii) consistencia entre medición y CFD (FLUENT) y con el estudio previo (diferencia del 27 % allí vs. 21,4 % acá); (iv) similitud geométrica con una laringe real (escala 7,5:1, dimensiones humanas). La validez de constructo respecto de la fonación real queda sin demostrar.

---

## 8. Análisis de los datos cuantitativos

**(a) Secuencia de análisis.**

1. Presentación gráfica de las distribuciones de presión (caída de presión vs. posición axial, Fig. 2) para cada presión transglótica y condición.
2. Comparación entre lados en el caso simétrico y luego en el oblicuo, tomando las diferencias como % de la presión transglótica.
3. Cálculo de medias y desviaciones estándar de esas diferencias sobre las cuatro presiones.
4. Comparación simétrica vs. oblicua, toma a toma.
5. Interpretación con CFD (líneas de corriente, perfiles de velocidad, contornos de presión) y con Bernoulli.
6. Discusión y contraste con el estudio previo.

**(b) ¿Interpreta hipótesis con pruebas estadísticas?** No. Las hipótesis implícitas se evalúan por comparación descriptiva de magnitudes, no por contraste inferencial.

**(c) Pruebas estadísticas empleadas.** Sólo estadística descriptiva: medias, desviaciones estándar y porcentajes relativos a la presión transglótica. No hay pruebas de hipótesis, intervalos de confianza ni análisis de varianza. Una mejora posible sería agregar intervalos de confianza o una prueba de diferencia de medias entre lados con repeticiones independientes.
