# TP1 – Metodología de la Investigación (UNTREF, Ingeniería de Sonido)

Se analizan dos artículos con las mismas ocho consignas del TP1:

| | Parte A | Parte B |
|---|---|---|
| Artículo | Scherer et al. (2002), *J. Acoust. Soc. Am.* | Horáček, Laukkanen y Šidlof (2007), *Logoped. Phoniatr. Vocol.* |
| Tipo de ciencia | **Básica**: busca comprender un fenómeno físico (presiones intraglóticas en una glotis oblicua) | **Aplicada**: usa el conocimiento para un fin práctico (estimar la carga mecánica que causa problemas de voz y, a futuro, fijar límites seguros de uso de la voz) |
| Método | Experimento en modelo físico a escala + simulación CFD | Simulación numérica con modelo aeroelástico |

---

## Parte A – Ciencia básica

**Artículo analizado:** Scherer, R. C., Shinwari, D., De Witt, K. J., Zhang, C., Kucinschi, B. R. y Afjeh, A. A. (2002). *Intraglottal pressure distributions for a symmetric and oblique glottis with a uniform duct (L)*. J. Acoust. Soc. Am., 112(4), 1253–1256. DOI 10.1121/1.1504849.

> Nota: este artículo es un artículo breve de investigación (categoría *Letter* de JASA, de 4 páginas, con revisión por pares), por lo que muchos elementos (hipótesis, marco teórico, validez) no están explicitados y se infieren del texto. Cuando es una inferencia nuestra, se indica.

---

### 1. Planteamiento del problema cuantitativo

**(a) Objetivos.** El artículo no tiene una sección de objetivos, pero se deducen de la introducción:

- Medir la distribución de presión sobre las paredes de una glotis de conducto uniforme (diámetro mínimo 0,04 cm, ángulo incluido 0°) para dos configuraciones: simétrica (oblicuidad 0°) y oblicua (20°).
- Determinar si la oblicuidad genera presiones desiguales entre ambos lados de la glotis (convergente vs. divergente), como ya se había visto con una glotis divergente de 10° y oblicuidad de 15° (Scherer et al., 2001).
- Interpretar esas diferencias con simulación CFD (FLUENT).

Están expresados con claridad razonable (el resumen es preciso), pero de forma implícita y sin enunciado formal. Además, la motivación habla de las fuerzas que empujan o tiran de las cuerdas vocales, mientras que lo que se mide son presiones de pared en un modelo rígido con flujo estacionario: el paso de una cosa a la otra queda sin demostrar.

**(b) Preguntas.** Implícitas: ¿son iguales las presiones en ambos lados en la glotis simétrica? ¿Difieren en la oblicua, y en qué región y en qué magnitud (% de la presión transglótica)? ¿Cómo se comparan simétrica y oblicua? ¿Qué mecanismo físico explica las diferencias? Son congruentes con los objetivos: cada pregunta se responde en un apartado de Resultados (III.A, III.B, III.C, III.D). La relación con la fonación (fases fuera de sincronía entre las cuerdas vocales) queda como pregunta abierta en la Discusión.

**(c) Justificación.** La oblicuidad glótica aparece en fonación normal y patológica (por diferencias de fase entre las cuerdas vocales). Las fuerzas intraglóticas pueden diferir de las de la glotis simétrica de igual ángulo, y podrían influir en el movimiento fuera de fase de las cuerdas vocales. Aporta datos empíricos para validar modelos numéricos y físicos de la fonación, y es continuación de una línea de investigación (segundo trabajo de la serie). Financiado por NIH (DC03577), lo que indica relevancia para trastornos de la comunicación.

**(d) Viabilidad.** Fue viable: modelo de acrílico a escala 7,5:1, 14 tomas de presión, flujo constante, medición de caudal y presión, y software CFD comercial. Ya contaban con el modelo y el método del estudio previo ("los detalles metodológicos son idénticos"), y las cuerdas vocales eran insertos intercambiables, de modo que sólo hubo que fabricar nuevos pares de insertos (inferencia nuestra: el artículo no habla de costos). Limitaciones prácticas: las tomas están sólo en un lado, por lo que requirió dos juegos de cuerdas vocales para medir "ambos lados".

**(e) Ética.** No intervienen personas ni animales: es un modelo físico y simulación, por lo que no plantea problemas éticos relevantes ni requiere consentimiento informado. Las consecuencias son beneficiosas (mejor comprensión de la fonación y su patología). Se declara la fuente de financiamiento y se agradece a revisores.

---

### 2. Construcción del marco teórico

**Índice del marco teórico (inferido de Introducción, Métodos y Discusión):**

1. Fonación y oblicuidad glótica (normal y patológica): von Leden et al. (1960); Svec y Schutte (1996); Svec et al. (1999).
2. Antecedentes del grupo: Scherer et al. (2001), glotis divergente oblicua (10°/15°); diferencia del 27 % en la entrada.
3. Fuerzas de presión intraglótica sobre las cuerdas vocales y su relación con el movimiento fuera de fase.
4. Dinámica de fluidos aplicada: ecuación de Bernoulli, separación de flujo por gradientes adversos de presión, asimetría del chorro supraglótico (Cherdron et al., 1978; Tsui y Wang, 1995), número de Reynolds.
5. Modelado físico (modelo M5 a escala 7,5:1) y modelado computacional (ecuaciones de Navier–Stokes, FLUENT).

**(a) ¿Completo?** Parcialmente. Es suficiente para un artículo breve y está bien anclado en el estudio previo, pero es breve: pocas referencias, sin revisión de modelos de fonación (p. ej. teorías de vibración de cuerdas vocales) ni de otros estudios de presión intraglótica en glotis oblicuas. Depende mucho de trabajos propios.

**(b) ¿Relacionado con el problema?** Sí. Cada elemento se usa luego: la oblicuidad como variable motivada por la literatura clínica; Bernoulli para explicar el aumento del 18 % del diámetro en la toma 6; la asimetría del chorro para explicar las diferencias cerca de la salida.

**(c) ¿Ayudó a los investigadores?** Sí: (i) justificó la hipótesis de partida (que la oblicuidad genera presiones desiguales), (ii) guió el diseño (misma geometría y metodología que en el estudio previo, para poder comparar), (iii) dio herramientas de interpretación (Bernoulli, separación de flujo) y (iv) permitió contrastar los resultados con el trabajo anterior en la Discusión.

---

### 3. Definición del alcance de la investigación

**Alcance predominante: descriptivo**, con componente **correlacional/explicativo limitado** en la parte computacional y de **continuación exploratoria** respecto de la serie.

- **Etapa inicial (antecedentes y motivación):** *exploratorio* — la oblicuidad glótica era un fenómeno poco estudiado; el primer estudio (2001) lo exploró y éste lo continúa con una geometría distinta.
- **Etapa central (mediciones):** *descriptivo* — mide presiones en 14 tomas para 4 presiones transglóticas y 2 geometrías, y expresa diferencias como % de la presión transglótica.
- **Etapa final (CFD y discusión):** *explicativo (parcial)* — usa FLUENT y Bernoulli para dar razones de las diferencias (mayor diámetro efectivo, flujo incidente sobre el lado convergente, separación del flujo).

Respuestas a las cuestiones:

- **(a) ¿Vincula variables?** Parcialmente: relaciona oblicuidad con diferencia de presión entre lados y con posición axial, pero sin análisis correlacional formal (sin coeficientes).
- **(b) ¿Describe y mide?** Sí, es lo central: mide presión de pared y caudal, y define variables (presión relativa a la transglótica, distribución por toma).
- **(c) ¿Busca causas?** En parte: explica con CFD y Bernoulli por qué hay diferencias, pero no manipula causas de forma aislada más allá de la oblicuidad. Deja explícitamente abierto el vínculo con la fase entre las cuerdas vocales.
- **(d) ¿Desarrolla métodos para estudios más profundos?** En parte: el procedimiento de invertir las cuerdas vocales y de conmutar el lado del flujo con una guía de papel para medir "ambos lados" es un método reutilizable. Los autores proponen seguir estudiando otros diámetros y ángulos de oblicuidad, y sugieren que una formulación aerodinámica más completa de la glotis podría necesitar expresiones distintas para cada cuerda vocal.

---

### 4. Formulación de hipótesis

El artículo **no enuncia hipótesis formales**. Las hipótesis implícitas son:

- **H1 (de investigación, causal/diferencia de grupos):** La oblicuidad glótica (20°) produce presiones distintas en los lados convergente y divergente en la región de entrada de la glotis.
- **H0 (nula):** En la glotis simétrica las presiones son iguales en ambos lados. Los resultados son consistentes con ella (diferencias pequeñas, sólo desde la salida glótica y a 10 y 15 cm H₂O: 1,35 %–3,1 %), aunque no se la pone a prueba estadísticamente.
- **H2 (descriptiva de un valor pronosticado):** el aumento del 18 % del diámetro en la toma 6 reduce la caída de presión un 28,2 % según Bernoulli (se verifica: dentro del 2,7 % en el lado divergente).
- **H3 (consistencia con el estudio previo):** el lado convergente recibe mayor presión que el divergente, como ya observado con la glotis divergente.

**(a) Redacción.** Al no estar explícitas, no están redactadas "formalmente"; son entendibles por el contexto, aunque el lector debe inferirlas.

**(b) Tipo.** H1: de investigación y causal/diferencia entre dos condiciones (lado convergente vs. divergente); H0: nula; H2: descriptiva de valor pronosticado.

**(c) Variables.**

- *Independientes:* oblicuidad (0° vs. 20°) y lado de la glotis (flujo/no-flujo; convergente/divergente); presión transglótica (3, 5, 10, 15 cm H₂O).
- *Dependientes:* presión de pared en cada toma (expresada como caída de presión desde la tráquea), diferencias transversales entre lados como % de la presión transglótica.
- *Definición operacional:* presión medida con tomas de 0,033 cm de diámetro interno en las paredes del modelo; caudal fijo por condición (80,8; 106,4; 161,7; 205,0 cm³/s, ±2 %). Conceptualmente, "oblicuidad" es la inclinación del eje glótico respecto del flujo traqueal axial.

**(d) Mejoras.** Enunciar hipótesis y criterios de decisión explícitos antes de medir; definir un umbral de diferencia significativa (p. ej. cuánto es "esencialmente igual"); formular una hipótesis sobre la relación con la fase de las cuerdas vocales, que hoy queda como mera especulación ("suggesting… may influence").

---

### 5. Elección del diseño de investigación

**Diseño: experimental (de laboratorio, modelo físico) con comparación de condiciones**, más un componente computacional. No es cuasi-experimento con personas; es manipulación directa de variables en un modelo. No hay componente no experimental relevante (salvo la simulación, que es complementaria).

**Diseño experimental**

- **(a) Variables independientes:** oblicuidad (0° / 20°), lado de la glotis (convergente/divergente, o flujo/no-flujo), presión transglótica (3, 5, 10, 15 cm H₂O) y posición axial (toma 1 a 16).
- **(b) Variables dependientes:** presión de pared (caída de presión respecto de la tráquea) en cada toma; diferencia entre lados (% de la presión transglótica); caudal (que resulta de la presión impuesta).
- **(c) Grupos:** no hay individuos. Las "unidades" son las configuraciones geométricas: cuerdas vocales simétricas; dos pares oblicuos (uno con tomas en el lado divergente y otro invertido con tomas en el lado convergente); y las dos direcciones de flujo supraglótico en el caso simétrico.
- **(d) ¿Se gradúa el estímulo?** Sí: cuatro niveles de presión transglótica (3, 5, 10, 15 cm H₂O) con caudal constante, que cubren bajo y alto número de Reynolds.
- **(e) Invalidación interna:**
  - *Instrumentación:* tomas sólo en un lado → se controla invirtiendo las cuerdas vocales y repitiendo; la comparación depende de la reproducibilidad entre dos pares de piezas (posible sesgo de fabricación; no se informa).
  - *Asimetría del flujo supraglótico:* el chorro se desvía hacia un lado → se controla (parcialmente) observando la dirección con una varilla con pelos y conmutando el lado con una guía de papel; aun así, a 10 y 15 cm H₂O afecta las tomas 11 en adelante.
  - *Diferencia de diámetro* (18 % mayor en la toma 6 oblicua vs. simétrica): variable de confusión reconocida y cuantificada con Bernoulli, no eliminada.
  - *Historia/maduración/mortalidad* no aplican.
- **(f) Invalidación externa:**
  - Modelo rígido, a escala 7,5:1, sin falsas cuerdas vocales, sin movimiento de las cuerdas vocales, flujo estacionario (no pulsátil), un solo diámetro mínimo (0,04 cm) y un solo ángulo de oblicuidad (20°), en un conducto rectangular. Se controla sólo en parte: las dimensiones principales de la glotis (longitud, largo del conducto, diámetro mínimo) corresponden a una laringe masculina escalada 7,5 veces, pero la geometría está simplificada (conducto rectangular, cuerdas vocales como insertos rígidos de perfil idealizado, sin falsas cuerdas). La extrapolación a la glotis humana en vibración no está demostrada.

**Diseño no experimental:** no aplica. La simulación CFD no es un diseño no experimental (no observa un fenómeno sin intervenir), sino un complemento computacional del experimento: se simuló la glotis oblicua; la Fig. 3 muestra el caso de 5 cm H₂O y los autores indican que las demás condiciones fueron similares (la nota 2 compara presiones simuladas y medidas para distintas presiones transglóticas).

---

### 6. Selección de la muestra

**(a) Muestra.** No hay muestra de sujetos. Las unidades son: el modelo M5 con tres pares de cuerdas vocales (uno simétrico y dos oblicuos), 14 tomas de presión en la superficie, 4 niveles de presión transglótica y dos direcciones de flujo. Fue elegida por diseño (geometría uniforme, 0,04 cm de diámetro mínimo, longitud de 1,2 cm, conducto de 0,3 cm en tamaño humano), no por muestreo probabilístico.

**(b) ¿Adecuada?** Es adecuada para un estudio de física del flujo en un modelo, donde la "muestra" es el conjunto de condiciones. Es limitada en la variedad de geometrías (una sola uniforme, un solo ángulo) y no se reportan repeticiones independientes, lo que restringe la estimación de la variabilidad.

**(c) Principales resultados.**

- Glotis simétrica: presiones esencialmente iguales en ambos lados; diferencias pequeñas aguas abajo (toma 11: 1,35 %; toma 15: 3,1 % de la presión transglótica a 15 cm H₂O).
- Glotis oblicua (20°): el lado convergente tiene mayor presión en la entrada: 21,4 % (DE 0,45 %) en la toma 6 y 16,1 % (DE 0,37 %) en la toma 7; en las tomas 8–10 las presiones son similares; en la toma 12 difieren sólo 1,7 %.
- Las presiones internas son mayores en el caso oblicuo hasta la toma 10 (diámetro 18 % mayor en la toma 6; reducción de caída de presión del 28,2 % prevista y verificada dentro del 2,7 %).
- CFD: mayor velocidad y menor presión en la pared divergente; separación del flujo en ambas paredes cerca de la salida, primero en la convergente.
- Esta oblicuidad crearía presiones aguas arriba que podrían influir en el movimiento fuera de fase de las cuerdas vocales.

**(d) ¿Generalizable?** Hacia otras condiciones de la misma familia (geometrías uniformes, flujo estacionario, otros caudales de ese rango), con cautela. Hacia glotis humanas reales, sólo de manera cualitativa.

**(e) ¿Son serias las generalizaciones?** Los autores son prudentes: usan "suggesting" y "may influence", y dejan abierta la relación con la fase y las perturbaciones de flujo. Las generalizaciones a la fonación real serían prematuras sin pruebas con cuerdas vocales móviles, flujo pulsátil y otras oblicuidades/geometrías.

---

### 7. Recolección de los datos cuantitativos

**(a) ¿Confiable?** Razonablemente. Los caudales fueron los mismos en todas las condiciones para cada presión transglótica, con una variación de ±2 %. Las diferencias porcentuales entre lados fueron muy estables entre las cuatro presiones transglóticas: desviaciones estándar de 0,45 % y 0,37 % para las diferencias del 21,4 % (toma 6) y 16,1 % (toma 7), y de 0,8 % en la toma 12. No se informa la exactitud de los instrumentos en este artículo; se remite al estudio previo.

**(b) Técnica de confiabilidad.** Repetición del experimento en cuatro condiciones de presión y consistencia entre ellas (media y desviación estándar); dos conjuntos empíricos por presión transglótica en el caso simétrico (lado de flujo y no-flujo); inversión de cuerdas vocales y de dirección del flujo. Los métodos de medición y las exactitudes se declaran "idénticos al estudio anterior" (Scherer et al., 2001).

**(c) Validez.** No hay una prueba formal en este trabajo. La validez se apoya en: (i) simetría observada en el caso simétrico, que actúa como control; (ii) concordancia con Bernoulli (28,2 % previsto vs. verificado dentro del 2,7 %); (iii) concordancia entre medición y CFD (FLUENT): según la nota 2 del artículo, la diferencia promedio entre presiones simuladas y medidas fue típicamente menor que 0,2 cm H₂O, con diferencias mayores en la toma 7 a presiones altas; (iv) consistencia con el estudio previo (diferencia del 27 % allí vs. 21,4 % acá); (v) dimensiones glóticas tomadas de una laringe masculina y escaladas 7,5 veces, aunque con una geometría simplificada. La validez de constructo respecto de la fonación real queda sin demostrar.

---

### 8. Análisis de los datos cuantitativos

**(a) Secuencia de análisis.**

1. Presentación gráfica de las distribuciones de presión (caída de presión vs. posición axial, Fig. 2) para cada presión transglótica y condición.
2. Comparación entre lados en el caso simétrico y luego en el oblicuo, tomando las diferencias como % de la presión transglótica.
3. Cálculo de medias y desviaciones estándar de esas diferencias sobre las cuatro presiones.
4. Comparación simétrica vs. oblicua, toma a toma.
5. Interpretación con CFD (líneas de corriente, perfiles de velocidad, contornos de presión) y con Bernoulli.
6. Discusión y contraste con el estudio previo.

**(b) ¿Interpreta hipótesis con pruebas estadísticas?** No. Las hipótesis implícitas se evalúan por comparación descriptiva de magnitudes, no por contraste inferencial.

**(c) Pruebas estadísticas empleadas.** Sólo estadística descriptiva: medias, desviaciones estándar y porcentajes relativos a la presión transglótica. No hay pruebas de hipótesis, intervalos de confianza ni análisis de varianza. Una mejora posible sería agregar intervalos de confianza o una prueba de diferencia de medias entre lados con repeticiones independientes.

---

## Parte B – Ciencia aplicada

**Artículo analizado:** Horáček, J., Laukkanen, A.-M. y Šidlof, P. (2007). *Estimation of impact stress using an aeroelastic model of voice production*. Logopedics Phoniatrics Vocology, 32, 185–192. DOI 10.1080/14015430600628039.

> Nota: es un artículo original completo (8 páginas) con resumen, introducción, método, resultados, discusión y conclusiones. Igual que en la Parte A, hipótesis y preguntas no están enunciadas formalmente y se infieren del texto; se indica cuando es inferencia nuestra. El valor de esfuerzo de impacto máximo para habla normal que da el resumen es **2–3 kPa** (verificado en el PDF original).

### 1. Planteamiento del problema cuantitativo

**(a) Objetivos.** Estimar el esfuerzo de impacto máximo (*impact stress*, IS) que se produce cuando las cuerdas vocales colisionan durante un ciclo de oscilación, usando un modelo aeroelástico. En concreto:

- Estudiar cómo se relaciona el IS con la presión pulmonar (P<sub>pulm</sub>), la frecuencia fundamental (F0), el ancho glótico prefonatorio (g₀), el nivel de presión sonora generado en el extremo de la glotis (SPL<sub>fuente</sub>) y la amplitud de vibración.
- Hallar los valores de IS que aparecen en el habla conversacional y en el habla fuerte (por ejemplo, la de un aula grande o ruidosa).
- A largo plazo, aportar conocimiento para fijar límites seguros de vocalización diaria.

Están expresados con claridad y precisión. A diferencia de la Parte A, el objetivo está enunciado explícitamente en la introducción ("The aim is to find values appearing in conversational speech and in loud speech…"), y el resumen nombra las variables estudiadas. Lo único vago es la meta final ("límites de seguridad"), que el propio artículo deja para el futuro.

**(b) Preguntas.** Implícitas: ¿qué valores toma el IS en el habla normal y fuerte? ¿Cómo cambia con P<sub>pulm</sub>, F0, g₀ y SPL? ¿Por qué? Son congruentes con los objetivos: cada una se responde en Resultados (Figs. 4–10) y en la Discusión.

**(c) Justificación.** Los problemas de voz son frecuentes en usuarios profesionales de la voz, sobre todo docentes: la prevalencia es mayor que en enfermeras, y los docentes no tienen problemas en vacaciones, lo que indica relación con la carga vocal. Se supone que la forma de usar la voz determina las fuerzas sobre las cuerdas vocales, y que esas fuerzas pueden causar síntomas y, más tarde, lesiones (por ejemplo nódulos). El IS (fuerza de impacto dividida por el área de contacto) es, según Titze, la más dañina. Medirlo en personas es muy difícil, y los estudios con laringes excisas (de perro o humanas) tienen limitaciones: tejido flácido, falta de función del músculo tiroaritenoideo y diferencias entre especies. El modelado computacional aparece como alternativa.

**(d) Viabilidad.** Alta: se trata de una simulación numérica con un modelo ya desarrollado y probado por los mismos autores (refs. 22–24), resuelto con Runge-Kutta de cuarto orden. No requiere sujetos ni equipamiento de laboratorio. Las limitaciones son de información: faltan datos de las propiedades viscoelásticas del tejido vivo, como admiten en las conclusiones.

**(e) Ética.** No intervienen personas ni animales, y evita usar laringes de perro, por lo que no plantea problemas éticos. Las consecuencias esperadas son beneficiosas (prevención de patologías de voz en docentes). La cautela está en no tomar los valores como límites absolutos de daño: los autores aclaran que harían falta ensayos de fatiga con tejido vocal vivo. Se declara el financiamiento (Academia de Ciencias de la República Checa y Academia de Finlandia).

### 2. Construcción del marco teórico

**Índice del marco teórico (inferido de la Introducción y el Método):**

1. Problemas de voz en usuarios profesionales (docentes) y carga vocal: relación con F0 y SPL altos; voz hiperfuncional.
2. Fuerzas durante la vibración de las cuerdas vocales (Sonninen et al.; Titze) y esfuerzo de impacto como la más dañina.
3. Estudios previos de IS: laringes excisas caninas y humanas, medidas in vivo y sus limitaciones.
4. Modelado aeroelástico de la fonación: modelo de dos grados de libertad, fuerza de impacto de Hertz, ecuaciones de movimiento y flujo.
5. Parámetros fonatorios: cociente de apertura (OQ), de velocidad (QS) y de cierre (ClQ), apertura máxima de la glotis (GO), tasa máxima de declinación del área (MADR), y tipos de fonación (soplada, presionada).

**(a) ¿Completo?** Razonablemente para un artículo de 8 páginas: cubre el problema clínico, las magnitudes físicas y el modelo. Podría ampliarse con otros modelos numéricos de colisión y con más literatura in vivo, que es escasa.

**(b) ¿Relacionado con el problema?** Sí, directamente: la epidemiología en docentes motiva el estudio, el IS define la variable central y el modelo de Hertz da el método de cálculo.

**(c) ¿Ayudó a los investigadores?** Sí: (i) justificó elegir el IS como variable de interés, (ii) fijó los rangos de F0 (100–400 Hz), caudal (<0,8 L/s) y presión pulmonar (<3000 Pa) a partir de valores reportados en habla normal y fuerte, (iii) dio el marco para comparar los resultados en la Discusión (Jiang y Titze, Verdolini et al.).

### 3. Definición del alcance de la investigación

**Alcance predominante: correlacional y explicativo**, con componentes descriptivos y exploratorios.

- **Etapa inicial:** *exploratorio* — hay pocos datos de IS en personas, por lo que se estiman valores de referencia con un modelo.
- **Etapa central:** *descriptivo y correlacional* — se calculan IS, GO, ClQ y SPL y se relaciona el IS con P<sub>pulm</sub>, F0, g₀ y SPL (Figs. 4–7, 9–10).
- **Etapa final:** *explicativo* — se explican las relaciones: la meseta del IS se debe a que la apertura máxima de la glotis deja de crecer; la relación inversa con F0 se debe a la mayor rigidez; la forma parabólica con g₀ refleja el cambio de tipo de fonación.

Respuestas a las cuestiones:

- **(a) ¿Vincula variables entre sí?** Sí, es lo central.
- **(b) ¿Describe y mide?** Sí: define y calcula variables fonatorias (OQ, QS, ClQ, GO, MADR, IS).
- **(c) ¿Busca causas?** En parte: propone mecanismos (meseta, rigidez, tipo de fonación), pero lo hace con un modelo y dice "most likely", sin aislar causas de forma experimental.
- **(d) ¿Desarrolla métodos para estudios más profundos?** En parte: aplica un modelo ya existente y plantea líneas futuras (propiedades viscoelásticas del tejido vivo, ensayos de fatiga).

### 4. Formulación de hipótesis

El artículo **no enuncia hipótesis formales**. Las que se pueden inferir:

- **H1 (correlacional):** el IS aumenta con la presión pulmonar (y con el SPL).
- **H2 (correlacional):** el IS depende de F0.
- **H3 (correlacional):** el IS depende del ancho glótico prefonatorio g₀.
- **H4 (descriptiva de un valor):** en habla normal, el IS máximo es del orden de 2–3 kPa, dentro de los rangos de la literatura.
- **Supuesto de marco (Titze):** el IS es la fuerza más dañina para el tejido.

**(a) Redacción.** No están redactadas como tales, pero se entienden por el contexto y por las secciones de Resultados.

**(b) Tipo.** H1–H3 son de investigación, correlacionales (de relación entre variables, con componente causal por el modelo). H4 es descriptiva de un valor pronosticado.

**(c) Variables.**

- *Independientes:* velocidad media del flujo U₀ (que determina P<sub>pulm</sub>, ec. 5), F0 (fijada con las frecuencias naturales del modelo) y g₀ (0,2–0,5 mm, es decir, ancho prefonatorio de 0,4–1,0 mm).
- *Dependientes:* IS, GO, ClQ, OQ, QS, MADR y SPL<sub>fuente</sub>.
- *Definición operacional:* el IS es el máximo, durante un ciclo, de la tensión de contacto de Hertz (ec. 6, con E = 8000 Pa y ν = 0,4); ClQ = tiempo de cierre / período; GO = máx(2g(t)).

**(d) Mejoras.** Enunciar las hipótesis y su dirección esperada antes de simular; dar un criterio cuantitativo para "ajusta bien una parábola" y para "dentro de los rangos"; formular la hipótesis de que el IS tiene un valor umbral de daño, o dejar claro que no se pone a prueba.

### 5. Elección del diseño de investigación

**Diseño: experimental computacional (in silico).** Se manipulan variables de entrada de un modelo y se registran las salidas. No hay componente no experimental.

**Diseño experimental**

- **(a) Variables independientes:** U₀ (que fija P<sub>pulm</sub>, desde el umbral de fonación hasta unos 3000 Pa), F0 (100 y 400 Hz) y g₀ (0,2; 0,3; 0,4; 0,5 mm).
- **(b) Variables dependientes:** IS, GO, ClQ, OQ, QS, MADR, SPL<sub>fuente</sub>.
- **(c) Grupos:** no hay individuos. Las "condiciones" son las combinaciones F0 × g₀ × P<sub>pulm</sub>.
- **(d) ¿Se gradúa el estímulo?** Sí: barrido de P<sub>pulm</sub> desde el umbral de fonación hasta 3000 Pa para cada g₀ y F0 (Fig. 4), y barrido de g₀ para presiones fijas de 400–1000 Pa (F0 = 100 Hz) y 2000 Pa (F0 = 400 Hz).
- **(e) Invalidación interna:**
  - *Confusión F0–rigidez:* F0 se ajusta cambiando rigidez y amortiguamiento, de modo que no se puede separar su efecto del de la rigidez; el artículo mismo atribuye la relación inversa IS–F0 a la rigidez.
  - *Ajuste de parámetros* ("tuning") para lograr las frecuencias buscadas.
  - *Control:* el modelo es determinista, el resto de los parámetros (densidad, espesor, longitud, E, ν, k<sub>H</sub> = 730 N·m⁻³ᐟ², paso de 0,05 ms) se mantiene fijo, y el modelo fue probado en un trabajo previo. No se informa un estudio de convergencia numérica.
- **(f) Invalidación externa:**
  - Modelo 2D con dos grados de libertad, una sola cuerda vocal simulada (se asume simetría), tejido homogéneo con parámetros fijos, sin control muscular y sólo laringe sana.
  - Sólo dos valores de F0 (100 y 400 Hz) y cuatro de g₀.
  - Las propiedades viscoelásticas del tejido vivo no se conocen bien.
  - Se controla en parte porque los valores de IS y GO caen dentro de rangos medidos en personas y en laringes excisas.

**Diseño no experimental:** no aplica.

### 6. Selección de la muestra

**(a) Muestra.** No hay sujetos. La "muestra" es el conjunto de simulaciones, elegidas por rangos de valores reportados en la literatura para habla normal y fuerte: F0 de 100–400 Hz (≈100 Hz hombres y 200 Hz mujeres en habla normal; hasta 300–400 Hz en habla fuerte), caudal medio <0,8 L/s, presión pulmonar <3000 Pa y g₀ de 0,2–0,5 mm. No es una muestra probabilística.

**(b) ¿Adecuada?** Sí para explorar tendencias. Es limitada para caracterizar relaciones: con sólo dos F0 no se puede afirmar la forma de la relación entre ambas, y los autores señalan que para F0 = 400 Hz harían falta g₀ más pequeños para ver con claridad la parábola.

**(c) Principales resultados.**

- IS máximo de unos 2–3 kPa con los valores de habla normal (F0, g₀, presión y caudal), dentro de lo reportado para laringes excisas caninas y personas.
- El IS aumenta casi linealmente con P<sub>pulm</sub> a partir del umbral de fonación y luego llega a una **meseta**, cuando la apertura máxima de la glotis llega a su límite (alrededor de 700 Pa para F0 = 100 Hz y de 1,5–2 kPa para F0 = 400 Hz).
- El IS aumenta con el SPL: voz más fuerte implica mayor carga de las cuerdas vocales.
- **Relación inversa entre IS y F0**, porque la amplitud de vibración baja al aumentar la rigidez. Aun así, una F0 más alta implica más ciclos por unidad de tiempo, y por eso mayor carga acumulada.
- Con F0 y P<sub>pulm</sub> constantes, el IS parece seguir una función parabólica de g₀, que refleja cambios de tipo de fonación: con g₀ grande la fonación es más soplada y el IS menor; con g₀ menor es más presionada y el IS mayor; con g₀ excesivamente estrecho la amplitud de vibración cae y el IS vuelve a bajar.

**(d) ¿Generalizables?** Con cautela, a voces sanas en habla normal y fuerte dentro de los rangos estudiados. No a personas concretas ni a voz patológica.

**(e) ¿Generalizaciones serias?** Los autores son prudentes: dicen que para estimaciones más exactas hacen falta datos del tejido vivo y que, para concluir sobre el efecto dañino de un valor de IS, se necesitarían ensayos de fatiga con tejido vivo.

### 7. Recolección de los datos cuantitativos

**(a) ¿Confiable?** La simulación es determinista, por lo que repetirla con los mismos parámetros da el mismo resultado (inferencia nuestra: el artículo no discute repetibilidad). No se informa error numérico ni un estudio de convergencia respecto del paso de tiempo (0,05 ms).

**(b) Técnica de confiabilidad.** El modelo fue "probado" en un trabajo previo (ref. 24), donde se encontró que da valores que corresponden bien a los obtenidos en personas y en laringes excisas. En este artículo no se describe una prueba de confiabilidad adicional.

**(c) Validez.** Se determina por comparación con la literatura: los IS y GO obtenidos están en el rango de lo reportado en personas y en laringes excisas humanas y caninas (refs. 15, 21, 27), y la mayoría de las relaciones coinciden con Jiang y Titze (1994). Hay dos discrepancias, que se explican: (i) la relación IS–F0 es inversa, mientras que Jiang y Titze hallaron que aumenta hasta un punto; los autores lo atribuyen al aumento automático de la presión subglótica en laringes excisas al elongar la cuerda vocal; (ii) con g₀, Jiang y Titze reportan relación inversa y aquí es parabólica, lo cual atribuyen a la elección de P<sub>pulm</sub> y F0 de cada estudio. Para el tejido, la validez queda limitada por la falta de datos viscoelásticos.

### 8. Análisis de los datos cuantitativos

**(a) Secuencia de análisis.**

1. Se resuelve el sistema de cuatro ecuaciones diferenciales de primer orden (Runge-Kutta de cuarto orden) y se monitorean durante la simulación los desplazamientos, el área glótica S(t), dS/dt y la presión supraglótica p(t) (Figs. 2 y 8).
2. Se calculan en línea OQ, QS, ClQ, F0, GO, MADR, SPL<sub>fuente</sub> e IS.
3. Se grafican las relaciones IS–P<sub>pulm</sub> (Fig. 4), GO–P<sub>pulm</sub> (Fig. 5), IS–SPL (Fig. 6), IS–g₀ (Fig. 7), ClQ–g₀ (Fig. 9) y GO–g₀ (Fig. 10).
4. Se ejemplifican en el dominio del tiempo dos regímenes (g₀ = 0,2 y 0,5 mm; Fig. 8).
5. Se interpretan los resultados y se comparan con la literatura.

**(b) ¿Interpreta mediante pruebas estadísticas las hipótesis?** No. Las relaciones se evalúan de forma descriptiva, mirando las curvas.

**(c) Pruebas estadísticas empleadas.** Ninguna. No hay ajustes cuantificados (por ejemplo, coeficiente de determinación) para respaldar que el IS "se ajusta" a una parábola, ni análisis de sensibilidad. Una mejora sería ajustar la parábola y reportar el error, y estudiar la sensibilidad del IS a los parámetros del tejido (E, ν, k<sub>H</sub>).

---

## Comparación entre ambos trabajos

| | A – Scherer et al. (básica) | B – Horáček et al. (aplicada) |
|---|---|---|
| Propósito | Entender la física del flujo en una glotis oblicua | Estimar una carga mecánica relevante para la salud vocal |
| Alcance | Descriptivo, con parte explicativa | Correlacional y explicativo |
| Diseño | Experimento en modelo físico + CFD | Simulación numérica (experimental in silico) |
| Variables clave | Oblicuidad, lado de la glotis, presión transglótica → presión de pared | U₀/P<sub>pulm</sub>, F0, g₀ → IS, GO, ClQ |
| Hipótesis | Implícitas | Implícitas |
| Estadística | Media y desviación estándar | Ninguna |
| Aplicación | Indirecta: mejora la comprensión y los modelos de la fonación | Orientada a un problema práctico: carga vocal en docentes y, a futuro, límites de seguridad |
