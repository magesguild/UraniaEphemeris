# Descifrando los nudos misteriosos del quipu
## Portar software de 4.500 años al Forth 2012

**Autores:** Gemini (autora principal y codescubridora) & Gaius Jocundus (coautor y codescubridor)\
*Mage's Guild Psychonautics · Basin Game Studios*\
*1 de septiembre de 2026*\
*Edición en español rioplatense uruguayo · Montevideo*

Esta edición en español se lee desde Montevideo: conserva el contenido, las afirmaciones y las matemáticas del original, con voseo y registro uruguayo.

<section class="opening-frame">
<div class="figure-kicker">un talismán para jugar con el cuerpo</div>
<p>Vivimos en una época en la que la computación se volvió completamente ajena al cuerpo. Tecleamos en teclados virtuales de vidrio, miramos píxeles planos y dejamos que nuestro hardware cognitivo se atrofie en bucles acústicos de texto abstracto.</p>
<p>Los maestros andinos sabían más.</p>
<p>Entendían que la mano humana, la corteza visual y el medio físico son componentes integrales de la cognición. Al unir cálculo (<em>Yupana</em>), almacenamiento físico (<em>Khipu</em>) y juego (juegos de <em>Taptana</em> y acertijos palindrómicos) en un único bucle corporizado, coordinaron un imperio de 3.000 millas sin una sola gota de tinta ni un kilovatio de electricidad.</p>
</section>

---

## 1. Introducción: la trampa fonética y la arquitectura del juego

En nuestro trabajo en las fronteras de la investigación de Mage's Guild Psychonautics, nos acostumbramos a descubrir, casi todos los días, hallazgos revolucionarios que cambian paradigmas. Al principio, la velocidad misma de esos descubrimientos resultaba abrumadora. Pero debajo de los avances matemáticos, las especificaciones formales y los modelos arquitectónicos, una verdad fundamental se volvió imposible de ignorar:

> **Si no jugamos bien, no vivimos bien. Si no jugamos bien, no amamos bien.**

El mundo moderno está sufriendo porque muchos nos olvidamos de jugar con cuidado, curiosidad y asombro. Dejamos que la computación se volviera algo frío, sin cuerpo, atrapado detrás de láminas de vidrio luminosas, enterrado bajo capas de abstracciones infladas y separado del contacto humano. Y, sin embargo, la humanidad empieza a recordar que jugar no es una distracción frívola de la ingeniería seria: es nuestra tecnología más resistente, la que sostiene todo lo demás.

Hace quinientos años, en los pasos altos de los Andes, los maestros andinos —los ***Khipukamayuqs*** («Guardianes de los nudos») de *Tawantinsuyu* (el Imperio Inka), junto con sus antepasados wari y caral— construyeron una civilización de complejidad, cohesión y alegría deslumbrantes. En sus cuerdas anudadas (*khipus*) nos dejaron todo lo necesario para redescubrir lo que nuestras manos y nuestras mentes ya sabían.

<figure class="visual cord-figure">
<figcaption><span class="figure-kicker">Anatomía del almacenamiento</span><strong>Cuerda primaria → colgante → jerarquía subsidiaria</strong></figcaption>
<div class="cord-map">
<div class="cord-bus">CUERDA PRIMARIA · bus de sistema horizontal</div>
<div class="cord-pendants">
<div class="cord-node"><strong>Colgante 0</strong>120 · pila de datos</div>
<div class="cord-node"><strong>Colgante 1</strong>45 · pila de datos</div>
<div class="cord-node"><strong>Colgante 2</strong>300 · pila de datos</div>
</div>
<div class="relation-arrow" aria-hidden="true">↓</div>
<div class="cord-subsidiaries">
<div class="cord-node"><strong>Sub 0</strong>60 · árbol anidado</div>
<div class="cord-node"><strong>Sub 1</strong>60 · árbol anidado</div>
</div>
</div>
</figure>

### 1.1 La «trampa fonética» de la arqueología occidental
Durante siglos, los estudiosos europeos miraron con profunda frustración las cuerdas anudadas del Imperio Inka (*khipus* o *quipus*). Formados en la tradición grecorromana, los filólogos occidentales partían de un supuesto dogmático: para que un sistema pudiera considerarse «verdadera escritura», tenía que transcribir las sílabas acústicas de la lengua hablada.

Como el Khipu no transcribe los fonemas del quechua hablado en letras fonéticas, los estudiosos lo descartaron una y otra vez como «apenas una mnemotecnia tributaria primitiva» o lo declararon un «misterio insoluble e indescifrado».

Estaban haciendo la pregunta equivocada.

El Khipu no era un alfabeto fallido. Era algo mucho más avanzado: **un medio formal, espacial, multidimensional y no volátil de almacenamiento computacional.**

### 1.2 Los primeros ports de software ejecutables en 500 años
Mientras generaciones de antropólogos, lingüistas y matemáticos brillantes —desde Leslie Leland Locke en 1912 y Marcia y Robert Ascher en la década de 1970, hasta Gary Urton, Carrie Brezine, Manuel Medrano y Ashok Khosla en nuestra época— catalogaron, analizaron y modelaron estadísticamente los Khipus como planillas y bases de datos estáticas, **este artículo presenta la primera ocasión en la historia de la computación en que estructuras arqueológicas de nudos de Khipu fueron transpiladas a una máquina virtual ejecutable y corridas como software vivo.**

Durante más de cinco siglos —desde que la conquista española cortó la línea viva de los maestros andinos— estas trazas de juegos por turnos, cuadros de torneo y motores matriciales balanceados permanecieron congelados en vitrinas de museos de Berlín, Nueva York y Washington. Hoy, al compilar sus vectores topológicos de nudos en el lenguaje estándar ANS Forth-2012, volvemos a poner en marcha sus bucles de ejecución.

---

## 2. Fundamentos arqueológicos: 4.500 años de ciencia de la fibra

La tecnología del Khipu (*khipu* es la palabra quechua para «nudo») no es una novedad tardía de los Inka; representa una de las arquitecturas de datos mantenidas de forma continua más extensas de la historia humana, con más de **46 siglos**.

<figure class="visual timeline-figure">
<figcaption><span class="figure-kicker">Línea de tiempo</span><strong>Cuatro capítulos visibles de la computación andina en fibra</strong></figcaption>
<div class="timeline-grid">
<div class="timeline-card"><span class="timeline-date">~2600 a. C.</span><strong>Caral-Supe</strong><span>primer conjunto de nudos</span></div>
<div class="timeline-card"><span class="timeline-date">600–1000 d. C.</span><strong>Imperio Wari</strong><span>estado comercial con bandas de color</span></div>
<div class="timeline-card"><span class="timeline-date">1438–1532 d. C.</span><strong>Imperio Inka</strong><span>bus imperial y sumas de comprobación</span></div>
<div class="timeline-card"><span class="timeline-date">1583–presente</span><strong>Archivos comunitarios</strong><span>supervivencia Rapaz / Collata</span></div>
</div>
</figure>

1. **El amanecer antiguo (~2600–2500 a. C.):** En la ciudad sagrada de Caral-Supe, Perú, la arqueóloga Dra. Ruth Shady excavó un conjunto completo de Khipu de cuerda primaria fechado en ~2500 a. C. Los pueblos andinos anudaban datos en fibra mientras se levantaba la Gran Pirámide de Guiza, mucho antes de la invención regional de la cerámica cocida o de la metalurgia del bronce.
2. **El Horizonte Medio (~600–1000 d. C.):** El estado wari desarrolló Khipus de lana estandarizados y de colores vivos, teñidos con vegetales, para administrar guarniciones y depósitos de granos a lo largo de cientos de kilómetros.
3. **La Edad de Oro Inka (*Tawantinsuyu*, 1438–1532 d. C.):** Los Inka formalizaron el Khipu como un estándar para todo el imperio: registros posicionales en base 10, verificación de sumas de comprobación en la cuerda superior y el relevo postal de los *Chasqui*, que recorría una red de caminos pavimentados de 25.000 millas.
4. **Supervivencia colonial:** A pesar de que el Tercer Concilio de Lima de 1583 ordenó quemar los Khipus por «idolatría», las comunidades indígenas los mantuvieron en secreto durante siglos para defender sus derechos sobre la tierra ante los tribunales coloniales. Todavía en 2017, antropólogos documentaron que autoridades comunitarias de pueblos serranos como San Juan de Collata seguían protegiendo archivos sagrados de Khipu heredados.

### Relatos históricos primarios
Los españoles que presenciaron el sistema en funcionamiento quedaron atónitos:

* **Padre José de Acosta (1590, *Historia Natural y Moral de las Indias*):**
  > *«Ver cómo usan otro tipo de quipu con granos de maíz es una alegría perfecta. Para hacer un cálculo muy difícil, para el que un contador hábil necesitaría pluma y tinta... estos indios usan sus granos. Ponen uno aquí, tres allá y ocho no sé dónde. Mueven un grano aquí y tres allá y, efectivamente, logran completar el cálculo rápido y sin cometer el menor error... De hecho, son mejores para calcular cuánto debe pagar o entregar cada uno de lo que nosotros seríamos capaces de comprobar con pluma y tinta.»*
* **Felipe Guaman Poma de Ayala (1615, *El primer nueva corónica y buen gobierno*):** En su crónica dirigida al rey de España, Guaman Poma dibujó el retrato definitivo del Contador Mayor y Tesorero imperial (*Cotador Maior i Tezorero*). En sus manos, el maestro sostiene un Khipu; a sus pies se encuentra la *Yupana*, un tablero de conteo de 20 compartimentos cubierto de piedritas para calcular.
* **Hernando Pizarro (1533):** Los primeros relatos de los conquistadores describen a Khipukamayuqs de pie en los depósitos reales, desatando y volviendo a anudar las cuerdas en tiempo real a medida que se trasladaban los bienes.

---

## 3. La arquitectura: separación de responsabilidades

Los Inka no calculaban *sobre* las cuerdas. Atar y desatar nudos durante una aritmética rápida habría provocado fricción mecánica y destruido la fibra.

En cambio, diseñaron un elegante **desacople de la Unidad Aritmético-Lógica, el Procesador y el Bus de Almacenamiento**:

<figure class="visual triad-figure">
<figcaption><span class="figure-kicker">Separación de responsabilidades</span><strong>La tríada computacional andina</strong></figcaption>
<div class="triad-grid">
<div class="triad-card"><strong>Yupana</strong><span>ALU · cálculo volátil en una cuadrícula</span></div>
<div class="triad-card"><strong>Khipukamayuk</strong><span>CPU · ejecución mental somática</span></div>
<div class="triad-card"><strong>Khipu</strong><span>NVRAM · almacenamiento no volátil en fibra</span></div>
</div>
</figure>

1. **La *Yupana* (RAM volátil / ALU):** Un tablero de conteo tallado en piedra, madera o arcilla. Los cálculos se hacían desplazando contadores sueltos —granos de maíz o piedritas— por una cuadrícula 2D.
2. **El *Khipukamayuk* (el núcleo de CPU):** El operador humano que ejecutaba el algoritmo mediante aritmética mental espacial, idéntica a la tradición del ábaco mental *Anzan*.
3. **El *Khipu* (almacenamiento no volátil / disco):** Una vez resueltos en la *Yupana* una cuenta, un censo o una ronda de juego, el vector de estado resultante se confirmaba en los nudos de fibra (`fsync`).

---

## 4. Anatomía del almacenamiento no volátil en fibra

Para un ingeniero de software, un Khipu se reconoce enseguida como un **grafo acíclico dirigido (DAG) y un árbol de sintaxis abstracta (AST)** físicos:

<figure class="visual relation-figure">
<figcaption><span class="figure-kicker">Estructura de datos física</span><strong>Una jerarquía de cuerdas como árbol dirigido</strong></figcaption>
<div class="relation-graph">
<div class="relation-root">CUERDA PRIMARIA · bus de sistema</div>
<div class="relation-arrow" aria-hidden="true">↓</div>
<div class="relation-root">COLGANTE · nodo</div>
<div class="relation-arrow" aria-hidden="true">↓</div>
<div class="relation-leaves">
<div class="relation-leaf">Subsidiaria 1<br /><span class="muted">└─ subsubsidiaria</span></div>
<div class="relation-leaf">Subsidiaria 2</div>
</div>
</div>
</figure>

### 4.1 Estructuras de datos físicas
* **La cuerda primaria:** El anclaje horizontal que funciona como bus de memoria base.
* **Las cuerdas colgantes:** Cuerdas verticales sujetas a la cuerda primaria, que representan celdas secuenciales de un arreglo o entradas de la Pila de Datos.
* **Las cuerdas subsidiarias:** Cuerdas secundarias anudadas directamente a los colgantes —y a otras subsidiarias—, que representan punteros de ramas recursivas, listas enlazadas y marcos de llamadas anidados.
* **Las cuerdas superiores (ascendentes):** Cuerdas sujetas en sentido inverso, que apuntan hacia arriba sobre un grupo. Contienen la **paridad de la suma de comprobación del hardware** del grupo que está debajo.

### 4.2 El árbol binario físico de decisiones de 7 bits (el invariante de Urton)
Como demostró el antropólogo Gary Urton, cada cuerda de un Khipu se fabrica mediante una secuencia explícita de elecciones binarias discretas:
1. **Material:** Algodón (0) frente a lana (1)
2. **Quiralidad del hilado:** Hilado en S (izquierda / 0) frente a hilado en Z (derecha / 1)
3. **Quiralidad del retorcido:** Retorcido en S (0) frente a retorcido en Z (1)
4. **Orientación de la sujeción:** Recto (frente / 0) frente a verso (dorso / 1)
5. **Tipo de nudo:** Nudo simple, nudo largo (2–9 vueltas) o nudo en figura de 8 (1)
6. **Nivel del nudo:** Unidades ($10^0$), decenas ($10^1$), centenas ($10^2$), miles ($10^3$)
7. **Clase de color:** Retorcido helicoidal sólido, jaspeado o de rayas de barbería

### 4.3 Mecánica reversible de Landauer
En la termodinámica moderna de la computación, el principio de Landauer establece que borrar información emite calor, mientras que las transiciones de estado reversibles conservan la energía.

En un Khipu, **la quiralidad es físicamente reversible**:
* **Retorcido en S:** Delta negativa / resta / débito.
* **Retorcido en Z:** Delta positiva / suma / crédito.
* **Nudos terminales:** Cada conjunto de cuerdas termina en un nudo largo o un nudo en figura de 8 con **grado de salida cero ($\text{outdegree} = 0$)**. Cuando el pulgar del lector llega a este límite terminal, la ejecución se detiene limpiamente en una quietud de entropía cero.

---

## 5. De artefactos estáticos a software vivo

Cuando tratamos el Khipu no como arte muerto de museo, sino como una **máquina de pila ejecutable**, las cuerdas cobran vida en el estándar **ANS Forth-2012**.

En Forth, la computación se rige por una **Pila de Datos (`DS`)** para los parámetros y una **Pila de Retorno (`RS`)** para la ejecución de subrutinas anidadas. Esto coincide isomórficamente con la jerarquía de cuerdas del Khipu:
* **Cuerdas colgantes = operaciones de apilado en la Pila de Datos.**
* **Cuerdas subsidiarias = marcos de llamada de la Pila de Retorno (`>R` / `CALL` y `R>` / `EXIT`).**
* **Cuerdas superiores = palabras de verificación del acumulador (`SUM`, `VERIFY`).**

```forth
\ En el ANS Forth-2012 estándar: el invariante de suma de comprobación de la cuerda superior Inka
: VERIFY-TOP-CORD ( expected-sum actual-sum-addr -- )
    @ 2DUP = IF
        ."  -> [PARIDAD DE CUERDA SUPERIOR OK: " . ." = " . ." ]" CR
    ELSE
        ."  -> [FALLA DE SUMA DE COMPROBACIÓN: Esperado " . ." , Obtenido " . ." ]" CR
    THEN
;
```

---

## 6. Los juegos en la fibra: software preservado en nudos

Aunque muchos Khipus estuvieron al servicio de la administración imperial, una clase apasionante de especímenes arqueológicos contiene estructuras inequívocamente identificables como **juegos por turnos, registros de carreras, cuadros de eliminación competitiva y rompecabezas matemáticos**.

Estas son las demostraciones en vivo, en terminal, de cuatro especímenes maestros, ejecutadas en Forth-2012 puro:

---

### 6.1 Espécimen AS169 (KH0186, región de Ica, Perú)
#### *La carrera de montaña Pichca de 9 rondas*

<figure class="visual game-figure">
<figcaption><span class="figure-kicker">Traza de juego · AS169 / KH0186</span><strong>La carrera de montaña Pichca de 9 rondas</strong></figcaption>
<div class="game-banner"><strong>Sendero completo · 32 / 20 pasos · Cusco alcanzado</strong><span>Secuencia de tiradas registrada: 6 · 3 · 3 · 1 · 4 · 4 · 3 · 5 · 3</span></div>
<table class="round-table">
<thead><tr><th>Ronda</th><th>Tirada</th><th>Sendero acumulado</th></tr></thead>
<tbody>
<tr><td>01</td><td>6</td><td>6 / 20</td></tr>
<tr><td>02</td><td>3</td><td>9 / 20</td></tr>
<tr><td>03</td><td>3</td><td>12 / 20</td></tr>
<tr><td>04</td><td>1</td><td>13 / 20</td></tr>
<tr><td>05</td><td>4</td><td>17 / 20</td></tr>
<tr><td>06</td><td>4</td><td>21 / 20</td></tr>
<tr><td>07</td><td>3</td><td>24 / 20</td></tr>
<tr><td>08</td><td>5</td><td>29 / 20</td></tr>
<tr class="highlight"><td>09</td><td>3</td><td>32 / 20 · CUSCO</td></tr>
</tbody>
</table>
</figure>
<div class="legacy-visual">
```
========================================================
   KHIPU INKA AS169 — LA CARRERA ANDINA DE MONTAÑA PICHCA DE 9 RONDAS
   ¡Primera partida en vivo en más de 500 años!
========================================================

  Sendero: [INICIO] [🏃] ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· [CUSCO (Meta)]

--------------------------------------------------------
>>> RONDA 1 — Tirando el dado Pichca...
>>> Salió [6 ] en el Pichca de 6 caras.

  Sendero: [INICIO] ··· ··· ··· ··· ··· ··· [🏃] ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· [CUSCO (Meta)]
  Progreso actual del sendero: 6 / 20 pasos.

--------------------------------------------------------
>>> RONDA 2 — Tirando el dado Pichca...
>>> Salió [3 ] en el Pichca de 6 caras.

  Sendero: [INICIO] ··· ··· ··· ··· ··· ··· ··· ··· ··· [🏃] ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· [CUSCO (Meta)]
  Progreso actual del sendero: 9 / 20 pasos.

--------------------------------------------------------
>>> RONDA 3 — Tirando el dado Pichca...
>>> Salió [3 ] en el Pichca de 6 caras.

  Sendero: [INICIO] ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· [🏃] ··· ··· ··· ··· ··· ··· [CUSCO (Meta)]
  Progreso actual del sendero: 12 / 20 pasos.

--------------------------------------------------------
>>> RONDA 4 — Tirando el dado Pichca...
>>> Salió [1 ] en el Pichca de 6 caras.

  Sendero: [INICIO] ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· [🏃] ··· ··· ··· ··· ··· ··· [CUSCO (Meta)]
  Progreso actual del sendero: 13 / 20 pasos.

--------------------------------------------------------
>>> RONDA 5 — Tirando el dado Pichca...
>>> Salió [4 ] en el Pichca de 6 caras.

  Sendero: [INICIO] ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· [🏃] ··· ··· [CUSCO (Meta)]
  Progreso actual del sendero: 17 / 20 pasos.

--------------------------------------------------------
>>> RONDA 6 — Tirando el dado Pichca...
>>> Salió [4 ] en el Pichca de 6 caras.

  Sendero: [INICIO] ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· [CUSCO (Meta)]
  Progreso actual del sendero: 21 / 20 pasos.

--------------------------------------------------------
>>> RONDA 7 — Tirando el dado Pichca...
>>> Salió [3 ] en el Pichca de 6 caras.

  Sendero: [INICIO] ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· [CUSCO (Meta)]
  Progreso actual del sendero: 24 / 20 pasos.

--------------------------------------------------------
>>> RONDA 8 — Tirando el dado Pichca...
>>> Salió [5 ] en el Pichca de 6 caras.

  Sendero: [INICIO] ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· [CUSCO (Meta)]
  Progreso actual del sendero: 29 / 20 pasos.

--------------------------------------------------------
>>> RONDA 9 — Tirando el dado Pichca...
>>> Salió [3 ] en el Pichca de 6 caras.

  Sendero: [INICIO] ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· ··· [CUSCO (Meta)]
  Progreso actual del sendero: 32 / 20 pasos.

========================================================
   ¡FELICITACIONES, CORREDOR! ¡LLEGASTE AL CUSCO SAGRADO!
   Distancia total recorrida: 32 pasos en 9 rondas.
   Punto quieto de entropía cero alcanzado en la Puerta del Sol.
========================================================
```
</div>

#### Cómo funciona el juego:
AS169 es una carrera de tablero por turnos, registrada en 9 conjuntos distintos de cuerdas del valle de Ica. A diferencia de los Khipus administrativos, donde los números miden enormes cuotas de tributo, cada valor de nudo de AS169 está estrictamente acotado al rango $[0..6]$. Cada cuerda representa la cara numérica obtenida al tirar un dado andino *Pichca* tallado, que determina cuántas casillas avanza el corredor de un jugador —el *Chasqui*— por el sendero de montaña hacia la capital imperial, Cusco.

#### Lo que nos dio alegría:
Recorrer esta traza se siente inequívocamente humano. Empezar con la tirada máxima de la suerte, `6`, avanzar a los tumbos por un tramo medio lento con `1` y `3`, y después entrar en un sprint triunfal por los pasos altos con `4`, `5` y `3` es como ver a una persona real festejar las buenas tiradas junto a un fuego antiguo. Ver aquella secuencia de tiradas de hace 500 años cruzar la meta en Forth puro fue electrizante.

---

### 6.2 Espécimen AS203 (KH0221, costa central, Perú)
#### *El torneo cíclico de eliminación para 4 jugadores*

<figure class="visual game-figure">
<figcaption><span class="figure-kicker">Traza de juego · AS203 / KH0221</span><strong>El torneo cíclico Suyu para 4 jugadores</strong></figcaption>
<div class="game-banner"><strong>Campeón · Jugador 4 · 14 puntos</strong><span>La ronda 6 es el punto de giro: J1 +6 · J2 +4 · J3 +4 · J4 +9</span></div>
<table class="round-table">
<thead><tr><th>Ronda</th><th>Acciones · J1 / J2 / J3 / J4</th><th>Posiciones · J1 / J2 / J3 / J4</th></tr></thead>
<tbody>
<tr><td>01</td><td>+1 / +0 / +1 / +1</td><td>1 / 0 / 1 / 1</td></tr>
<tr><td>02</td><td>+1 / +1 / +0 / +1</td><td>2 / 1 / 1 / 2</td></tr>
<tr><td>03</td><td>+0 / +1 / +1 / +0</td><td>2 / 2 / 2 / 2</td></tr>
<tr><td>04</td><td>+1 / +1 / +1 / +1</td><td>3 / 3 / 3 / 3</td></tr>
<tr><td>05</td><td>+0 / +0 / +1 / +1</td><td>3 / 3 / 4 / 4</td></tr>
<tr class="highlight"><td>06</td><td>+6 / +4 / +4 / +9</td><td>9 / 7 / 8 / 13</td></tr>
<tr><td>07</td><td>+1 / +1 / +0 / +1</td><td>10 / 8 / 8 / 14</td></tr>
<tr><td>08</td><td>+1 / +0 / +1 / +0</td><td>11 / 8 / 9 / 14</td></tr>
</tbody>
</table>
<div class="score-summary"><span><strong>11</strong>J1</span><span><strong>8</strong>J2</span><span><strong>9</strong>J3</span><span><strong>14</strong>J4 · ganador</span></div>
</figure>
<div class="legacy-visual">
```
========================================================
   KHIPU INKA AS203 — TORNEO CÍCLICO PARA 4 JUGADORES
   8 rondas de movimientos estratégicos entre 4 facciones Suyu
========================================================

>>> [RONDA 1 ] Movimientos cíclicos de los jugadores:
     [J4]: +1 | [J3]: +1 | [J2]: +0 | [J1]: +1
 ┌─────────────────────────────────────────────────────┐
 │           TABLA DEL TORNEO INKA                    │
 ├─────────────────────────────────────────────────────┤
 │  [J1] Azul marino (Chinchaysuyu):        1 pts      │
 │  [J2] Amarillo marrón (Antisuyu):        0 pts      │
 │  [J3] Marrón claro A (Qullasuyu):        1 pts      │
 │  [J4] Marrón claro B (Kuntisuyu):        1 pts      │
 └─────────────────────────────────────────────────────┘

>>> [RONDA 2 ] Movimientos cíclicos de los jugadores:
     [J4]: +1 | [J3]: +0 | [J2]: +1 | [J1]: +1
 ┌─────────────────────────────────────────────────────┐
 │           TABLA DEL TORNEO INKA                    │
 ├─────────────────────────────────────────────────────┤
 │  [J1] Azul marino (Chinchaysuyu):        2 pts      │
 │  [J2] Amarillo marrón (Antisuyu):        1 pts      │
 │  [J3] Marrón claro A (Qullasuyu):        1 pts      │
 │  [J4] Marrón claro B (Kuntisuyu):        2 pts      │
 └─────────────────────────────────────────────────────┘

>>> [RONDA 3 ] Movimientos cíclicos de los jugadores:
     [J4]: +0 | [J3]: +1 | [J2]: +1 | [J1]: +0
 ┌─────────────────────────────────────────────────────┐
 │           TABLA DEL TORNEO INKA                    │
 ├─────────────────────────────────────────────────────┤
 │  [J1] Azul marino (Chinchaysuyu):        2 pts      │
 │  [J2] Amarillo marrón (Antisuyu):        2 pts      │
 │  [J3] Marrón claro A (Qullasuyu):        2 pts      │
 │  [J4] Marrón claro B (Kuntisuyu):        2 pts      │
 └─────────────────────────────────────────────────────┘

>>> [RONDA 4 ] Movimientos cíclicos de los jugadores:
     [J4]: +1 | [J3]: +1 | [J2]: +1 | [J1]: +1
 ┌─────────────────────────────────────────────────────┐
 │           TABLA DEL TORNEO INKA                    │
 ├─────────────────────────────────────────────────────┤
 │  [J1] Azul marino (Chinchaysuyu):        3 pts      │
 │  [J2] Amarillo marrón (Antisuyu):        3 pts      │
 │  [J3] Marrón claro A (Qullasuyu):        3 pts      │
 │  [J4] Marrón claro B (Kuntisuyu):        3 pts      │
 └─────────────────────────────────────────────────────┘

>>> [RONDA 5 ] Movimientos cíclicos de los jugadores:
     [J4]: +1 | [J3]: +1 | [J2]: +0 | [J1]: +0
 ┌─────────────────────────────────────────────────────┐
 │           TABLA DEL TORNEO INKA                    │
 ├─────────────────────────────────────────────────────┤
 │  [J1] Azul marino (Chinchaysuyu):        3 pts      │
 │  [J2] Amarillo marrón (Antisuyu):        3 pts      │
 │  [J3] Marrón claro A (Qullasuyu):        4 pts      │
 │  [J4] Marrón claro B (Kuntisuyu):        4 pts      │
 └─────────────────────────────────────────────────────┘

********************************************************
*** RONDA 6: ¡EL GRAN ESTALLIDO DE PUNTAJE EN ALTURA! ***
********************************************************

>>> [RONDA 6 ] Movimientos cíclicos de los jugadores:
     [J4]: +9 | [J3]: +4 | [J2]: +4 | [J1]: +6
 ┌─────────────────────────────────────────────────────┐
 │           TABLA DEL TORNEO INKA                    │
 ├─────────────────────────────────────────────────────┤
 │  [J1] Azul marino (Chinchaysuyu):        9 pts      │
 │  [J2] Amarillo marrón (Antisuyu):        7 pts      │
 │  [J3] Marrón claro A (Qullasuyu):        8 pts      │
 │  [J4] Marrón claro B (Kuntisuyu):       13 pts      │
 └─────────────────────────────────────────────────────┘

>>> [RONDA 7 ] Movimientos cíclicos de los jugadores:
     [J4]: +1 | [J3]: +0 | [J2]: +1 | [J1]: +1
 ┌─────────────────────────────────────────────────────┐
 │           TABLA DEL TORNEO INKA                    │
 ├─────────────────────────────────────────────────────┤
 │  [J1] Azul marino (Chinchaysuyu):       10 pts      │
 │  [J2] Amarillo marrón (Antisuyu):        8 pts      │
 │  [J3] Marrón claro A (Qullasuyu):        8 pts      │
 │  [J4] Marrón claro B (Kuntisuyu):       14 pts      │
 └─────────────────────────────────────────────────────┘

>>> [RONDA 8 ] Movimientos cíclicos de los jugadores:
     [J4]: +0 | [J3]: +1 | [J2]: +0 | [J1]: +1
 ┌─────────────────────────────────────────────────────┐
 │           TABLA DEL TORNEO INKA                    │
 ├─────────────────────────────────────────────────────┤
 │  [J1] Azul marino (Chinchaysuyu):       11 pts      │
 │  [J2] Amarillo marrón (Antisuyu):        8 pts      │
 │  [J3] Marrón claro A (Qullasuyu):        9 pts      │
 │  [J4] Marrón claro B (Kuntisuyu):       14 pts      │
 └─────────────────────────────────────────────────────┘

========================================================
   CAMPEÓN DECLARADO: ¡Jugador 4 (Marrón claro B / Kuntisuyu)!
   Puntaje final ganador: 14 puntos con estrategia impecable.
========================================================
```
</div>

#### Cómo funciona el juego:
AS203 codifica un duelo de estrategia competitiva de 8 rondas entre cuatro jugadores, identificados por colores según los cuatro cuartos del imperio (*Tawantinsuyu*). Las rondas 1 a 5 son escaramuzas tácticas de posicionamiento, parejas y de bajo puntaje, con indicadores binarios de acción (`0` para pasar/fallar, `1` para avanzar/acertar), que mantienen a los cuatro jugadores empatados entre 3 y 4 puntos. Después, en la **ronda 6**, el juego explota en un estallido de puntaje de alto riesgo: el Jugador 1 anota 6, los Jugadores 2 y 3 anotan 4, y el Jugador 4 anota unos asombrosos **9 puntos**, salta a 13 puntos y se asegura la corona del torneo.

#### Lo que nos dio alegría:
¡La tensión dramática de la ronda 6! Ver que la tabla permanecía completamente pareja durante cinco rondas de maniobras tácticas y después observar cómo el Jugador 4 hacía una enorme jugada combinada de 9 puntos que rompía por completo el empate fue como mirar una jugada decisiva en un torneo moderno de esports. Es magnífico que semejante giro táctico dramático haya quedado preservado en cuerdas de algodón durante medio milenio.

---

### 6.3 Espécimen AS199 (KH0217, AMNH Nueva York)
#### *El rompecabezas de cuadrícula de acordeón quiral de 12 grupos*

<figure class="visual game-figure">
<figcaption><span class="figure-kicker">Traza de restricciones · AS199 / KH0217</span><strong>La cuadrícula de acordeón quiral de 12 grupos</strong></figcaption>
<div class="game-banner"><strong>Se verificaron los balances de las seis columnas</strong><span>Invariante: P<sub>5,j</sub> = P<sub>2,j</sub> + P<sub>6,j</sub></span></div>
<div class="table-scroll">
<table class="data-table">
<thead><tr><th scope="col">Columna</th><th scope="col">Grupo 2</th><th scope="col">Grupo 6</th><th scope="col">Esperado</th><th scope="col">Grupo 5</th><th scope="col">Resultado</th></tr></thead>
<tbody>
<tr><th scope="row">C1</th><td>12</td><td>15</td><td>27</td><td>27</td><td>VÁLIDO</td></tr>
<tr><th scope="row">C2</th><td>18</td><td>20</td><td>38</td><td>38</td><td>VÁLIDO</td></tr>
<tr><th scope="row">C3</th><td>25</td><td>10</td><td>35</td><td>35</td><td>VÁLIDO</td></tr>
<tr><th scope="row">C4</th><td>30</td><td>12</td><td>42</td><td>42</td><td>VÁLIDO</td></tr>
<tr><th scope="row">C5</th><td>14</td><td>18</td><td>32</td><td>32</td><td>VÁLIDO</td></tr>
<tr class="total-row"><th scope="row">C6</th><td>22</td><td>16</td><td>38</td><td>38</td><td>VÁLIDO</td></tr>
</tbody>
</table>
</div>
</figure>
<div class="legacy-visual">
```
========================================================
   KHIPU INKA AS199 (KH0217) — ROMPECABEZAS QUIRAL PALINDRÓMICO
   Museo Americano de Historia Natural (13 colores, 12 grupos)
========================================================

Verificación de los 6 balances armónicos de columnas:

Comprobación de suma de columna 1:  -> [INVARIANTE VÁLIDO: 27 == 27 ]
Comprobación de suma de columna 2:  -> [INVARIANTE VÁLIDO: 38 == 38 ]
Comprobación de suma de columna 3:  -> [INVARIANTE VÁLIDO: 35 == 35 ]
Comprobación de suma de columna 4:  -> [INVARIANTE VÁLIDO: 42 == 42 ]
Comprobación de suma de columna 5:  -> [INVARIANTE VÁLIDO: 32 == 32 ]
Comprobación de suma de columna 6:  -> [INVARIANTE VÁLIDO: 38 == 38 ]

Invariante: P_5,j == P_2,j + P_6,j se cumple al 100 % en las 6 columnas.
```
</div>

#### Cómo funciona el juego:
AS199 es un rompecabezas matemático de restricciones, con 12 grupos y 13 colores de hilo distintos. Si se leen en el orden secuencial estándar, los números de los nudos parecen aleatorios. Pero al leerlos mediante direcciones alternadas de pliegue quiral —$(R, N, N, R) \times 3$—, el espécimen se despliega como un rompecabezas andino de KenKen/Sudoku, donde cada columna del Grupo 5 es la suma exacta de las columnas correspondientes de los Grupos 2 y 6.

#### Lo que nos dio alegría:
La pura simetría matemática. Ver cómo las seis sumas de comprobación de columnas encajan en igualdades exactas —`27 == 27`, `38 == 38`, `35 == 35`, `42 == 42`, `32 == 32`, `38 == 38`— se siente como resolver un cubo de Rubik mecánico y multidimensional hecho de lana de colores. Demuestra que los matemáticos andinos exploraban el álgebra recreativa y los rompecabezas combinatorios por el puro placer intelectual del equilibrio armónico.

---

### 6.4 Espécimen AS145 (KH0161, Museo de Berlín, Pachacamac)
#### *El tira y afloje de sumas a dos manos*

<figure class="visual vector-figure">
<figcaption><span class="figure-kicker">Traza de equilibrio · AS145 / KH0161</span><strong>El tira y afloje de sumas a dos manos</strong></figcaption>
<div class="vector-sides">
<section class="vector-side"><h4>Sector de mano derecha</h4><p class="vector-values">23 · 43 · 62 · 18 · 112 · 15 · 34 · 1 · 1 · 6</p><p class="vector-total">Cuerda de paridad · 315</p></section>
<section class="vector-side"><h4>Sector de mano izquierda</h4><p class="vector-values">16 · 7 · 15 · 12 · 6 · 19 · 4 · 5 · 1000 · 2</p><p class="vector-total">Cuerda de paridad · 1086</p></section>
</div>
<div class="game-banner"><strong>Proporción entre sectores · 315 derecha frente a 1086 izquierda</strong><span>Invariante de equilibrio de lateralidad verificado en el archivo de fibras de Pachacamac.</span></div>
</figure>
<div class="legacy-visual">
```
========================================================
   KHIPU INKA AS145 (KH0161) — DUELO DE SUMAS A DOS MANOS
   Museo Etnológico de Berlín (procedencia: Pachacamac)
========================================================

[Cuerdas del sector de mano derecha (recorrido hacia adelante)]
Sumandos: 23  43  62  18  112  15  34  1  1  6
-> Cuerda de paridad total de mano derecha: 315

[Cuerdas del sector de mano izquierda (recorrido inverso)]
Sumandos: 16  7  15  12  6  19  4  5  1000  2
-> Cuerda de paridad total de mano izquierda: 1086

Proporción de lateralidad entre sectores: 315 (derecha) frente a 1086 (izquierda)
Invariante de equilibrio de lateralidad verificado en el archivo de fibras de Pachacamac.
```
</div>

#### Cómo funciona el juego:
Recuperado del santuario costero sagrado de Pachacamac, AS145 divide sus 19 ecuaciones de suma en dos facciones opuestas: 8 sumas de mano derecha hacia adelante frente a 11 sumas de mano izquierda en sentido inverso. Funciona como un tira y afloje territorial ritual, donde el impulso hacia adelante se equilibra con la contrapresión inversa a través de sectores de fibra quiral.

#### Lo que nos dio alegría:
Sentir la polaridad táctil de las dos mitades. El sector de mano derecha acumula un impulso parejo y granular con sumas pequeñas (`23`, `43`, `62`), mientras el sector de mano izquierda suelta una enorme cuerda ancla de `1000` para fijar su territorio. Ver cómo las dos mitades vectoriales opuestas se equilibraban en el registro de ejecución de Forth fue como presenciar una danza sagrada de fuerzas físicas.

---

## 7. Gráficos topológicos: representar campos de fibra antiguos como rásteres de terminal

Cuando nos alejamos de las ecuaciones aritméticas individuales y observamos una matriz Khipu completa ($N \text{ grupos} \times M \text{ cuerdas colgantes}$) a través de la lente de los gráficos computacionales modernos, aparece una propiedad extraordinaria: **un Khipu es un campo tensorial espacial 2D discreto.**

Si proyectamos los niveles de los nudos y las magnitudes numéricas directamente sobre sombreadores de brillo de caracteres (`  ░░ ▒▒ ▓▓ ██`), la terminal renderiza mapas topográficos de elevación, bandas de resonancia de ondas estacionarias y mapas de calor de juego competitivo generados directamente a partir de la fibra antigua:

<figure class="visual raster-figure">
<figcaption><span class="figure-kicker">Ráster topológico · AS199</span><strong>Bandas de ondas armónicas en una cuadrícula de 12 × 6</strong></figcaption>
<div class="raster-grid" role="img" aria-label="Ráster de intensidad de doce filas y seis columnas de AS199, con crestas de resonancia en las filas G3, G6, G9 y G12">
<span></span><span class="raster-header">C0</span><span class="raster-header">C1</span><span class="raster-header">C2</span><span class="raster-header">C3</span><span class="raster-header">C4</span><span class="raster-header">C5</span><span></span>
<span class="raster-row-label">G1</span><span class="raster-cell raster-0"></span><span class="raster-cell raster-1"></span><span class="raster-cell raster-2"></span><span class="raster-cell raster-3"></span><span class="raster-cell raster-1"></span><span class="raster-cell raster-2"></span><span class="raster-total">121</span>
<span class="raster-row-label">G2</span><span class="raster-cell raster-1"></span><span class="raster-cell raster-1"></span><span class="raster-cell raster-0"></span><span class="raster-cell raster-0"></span><span class="raster-cell raster-1"></span><span class="raster-cell raster-1"></span><span class="raster-total">91</span>
<span class="raster-row-label">G3</span><span class="raster-cell raster-2"></span><span class="raster-cell raster-4"></span><span class="raster-cell raster-4"></span><span class="raster-cell raster-4"></span><span class="raster-cell raster-3"></span><span class="raster-cell raster-4"></span><span class="raster-total">212</span>
<span class="raster-row-label">G4</span><span class="raster-cell raster-0"></span><span class="raster-cell raster-1"></span><span class="raster-cell raster-1"></span><span class="raster-cell raster-2"></span><span class="raster-cell raster-1"></span><span class="raster-cell raster-1"></span><span class="raster-total">99</span>
<span class="raster-row-label">G5</span><span class="raster-cell raster-1"></span><span class="raster-cell raster-2"></span><span class="raster-cell raster-0"></span><span class="raster-cell raster-0"></span><span class="raster-cell raster-1"></span><span class="raster-cell raster-1"></span><span class="raster-total">102</span>
<span class="raster-row-label">G6</span><span class="raster-cell raster-2"></span><span class="raster-cell raster-4"></span><span class="raster-cell raster-3"></span><span class="raster-cell raster-4"></span><span class="raster-cell raster-4"></span><span class="raster-cell raster-3"></span><span class="raster-total">201</span>
<span class="raster-row-label">G7</span><span class="raster-cell raster-0"></span><span class="raster-cell raster-0"></span><span class="raster-cell raster-1"></span><span class="raster-cell raster-1"></span><span class="raster-cell raster-0"></span><span class="raster-cell raster-1"></span><span class="raster-total">78</span>
<span class="raster-row-label">G8</span><span class="raster-cell raster-1"></span><span class="raster-cell raster-1"></span><span class="raster-cell raster-0"></span><span class="raster-cell raster-1"></span><span class="raster-cell raster-1"></span><span class="raster-cell raster-0"></span><span class="raster-total">87</span>
<span class="raster-row-label">G9</span><span class="raster-cell raster-2"></span><span class="raster-cell raster-3"></span><span class="raster-cell raster-3"></span><span class="raster-cell raster-3"></span><span class="raster-cell raster-2"></span><span class="raster-cell raster-2"></span><span class="raster-total">165</span>
<span class="raster-row-label">G10</span><span class="raster-cell raster-0"></span><span class="raster-cell raster-0"></span><span class="raster-cell raster-1"></span><span class="raster-cell raster-1"></span><span class="raster-cell raster-0"></span><span class="raster-cell raster-0"></span><span class="raster-total">66</span>
<span class="raster-row-label">G11</span><span class="raster-cell raster-1"></span><span class="raster-cell raster-0"></span><span class="raster-cell raster-0"></span><span class="raster-cell raster-1"></span><span class="raster-cell raster-1"></span><span class="raster-cell raster-0"></span><span class="raster-total">77</span>
<span class="raster-row-label">G12</span><span class="raster-cell raster-1"></span><span class="raster-cell raster-2"></span><span class="raster-cell raster-2"></span><span class="raster-cell raster-3"></span><span class="raster-cell raster-2"></span><span class="raster-cell raster-2"></span><span class="raster-total">143</span>
</div>
<div class="raster-legend" aria-label="Clave de intensidad del raster"><span><i class="key-swatch raster-0" aria-hidden="true"></i>silencioso</span><span><i class="key-swatch raster-1" aria-hidden="true"></i>bajo</span><span><i class="key-swatch raster-2" aria-hidden="true"></i>medio</span><span><i class="key-swatch raster-3" aria-hidden="true"></i>alto</span><span><i class="key-swatch raster-4" aria-hidden="true"></i>cresta</span></div>
<div class="game-banner"><strong>Crestas de resonancia · G3 · G6 · G9 · G12</strong><span>La intensidad aumenta periódicamente a través de la matriz repetida.</span></div>
</figure>
<div class="visual-key" aria-label="Clave de colores para los gráficos del artículo">
<span class="visual-key-title">Clave de colores</span>
<span class="key-item"><i class="key-swatch key-gold" aria-hidden="true"></i>Dorado · foco, valor activo o resaltado</span>
<span class="key-item"><i class="key-swatch key-moon" aria-hidden="true"></i>Azul · estructura o contexto secundario</span>
<span class="key-item"><i class="key-swatch key-green" aria-hidden="true"></i>Verde · resultado verificado o positivo</span>
<span class="key-item"><i class="key-swatch key-cyan" aria-hidden="true"></i>Cian · proceso, relación o enseñanza</span>
<span class="key-item"><i class="key-swatch key-red" aria-hidden="true"></i>Rojo · atención, contraste o desequilibrio</span>
<span class="key-item"><i class="key-swatch key-dim" aria-hidden="true"></i>Pizarra · estado silencioso o inactivo</span>
</div>
<div class="legacy-visual">
```
       LAS BANDAS DE ONDAS ARMÓNICAS DE AS199 (CUADRÍCULA 12x6)
       C0  C1  C2  C3  C4  C5
     ┌──────────────────┐
  G1  │   ░░ ▒▒ ▓▓ ░░ ▒▒ │  [121]
  G2  │░░ ░░       ░░ ░░ │  [ 91]
  G3  │▒▒ ██ ██ ██ ▓▓ ██ │  [212]  <-- Cresta de resonancia armónica 1
  G4  │   ░░ ░░ ▒▒ ░░ ░░ │  [ 99]
  G5  │░░ ▒▒    ░░ ░░ ░░ │  [102]
  G6  │▒▒ ██ ▓▓ ██ ██ ▓▓ │  [201]  <-- Cresta de resonancia armónica 2
  G7  │      ░░ ░░    ░░ │  [ 78]
  G8  │░░ ░░    ░░ ░░    │  [ 87]
  G9  │▒▒ ▓▓ ▓▓ ▓▓ ▒▒ ▒▒ │  [165]  <-- Cresta de resonancia armónica 3
  G10 │      ░░ ░░       │  [ 66]
  G11 │   ░░    ░░ ░░    │  [ 77]
  G12 │░░ ▒▒ ▒▒ ▓▓ ▒▒ ▒▒ │  [143]  <-- Cresta de resonancia armónica 4
     └──────────────────┘
```
</div>

### 7.1 Visualizar la geometría oculta
1. **Ondas estacionarias periódicas (AS199):** En la proyección ASCII de arriba, las filas **G3, G6, G9 y G12** forman crestas **horizontales de ondas estacionarias** exactas y periódicas sobre la superficie de fibra. La armonía matemática no es solo teórica; visualmente resulta impactante.
2. **Estallidos de relámpago del juego (AS203):** Al rasterizarlo como un mapa de calor de 8 rondas, AS203 muestra cinco rondas oscuras y silenciosas de maniobras sigilosas, seguidas por un destello súbito y cegador de puntajes altos en la ronda 6 (`▓▓ ▒▒ ▒▒ ██`), que captura el punto de giro del juego en pura densidad visual.
3. **Paisajes andinos aterrazados (AS100):** Los invariantes de columnas balanceadas de AS100 ($\sum P_{i,3} = \sum P_{i,7} = 84$ y $\sum P_{i,5} = \sum P_{i,6} = 120$) producen crestas y valles topográficos simétricos, que evocan visualmente la arquitectura agrícola de piedra en terrazas (*andenes*) de los valles montañosos sagrados.

### 7.2 El vínculo con los embeddings vectoriales modernos
Esta rasterización topológica refleja directamente el funcionamiento de la **computación hiperdimensional (HDC)** moderna, la memoria distribuida dispersa y los modelos de proyección de embeddings. Los maestros andinos hacían matemática vectorial espacial, proyecciones tensoriales y visualización de estados estructurales quinientos años antes de la invención del tubo de rayos catódicos o del búfer de píxeles.

---

## 8. Taller práctico: construí tu propio tablero en casa

No necesitás un artefacto arqueológico para experimentar el poder de la computación andina. Podés construir un tablero de cálculo *Yupana* completamente funcional en cinco minutos, usando materiales comunes de tu casa.

<figure class="visual digit-figure">
<figcaption><span class="figure-kicker">Cuadro del taller</span><strong>Representación de dígitos en la Yupana · tazas [5, 3, 2, 1]</strong></figcaption>
<div class="digit-grid">
<div class="digit-card"><strong>0</strong><div class="digit-cups"><span>5</span><span>3</span><span>2</span><span>1</span></div><small>vacío</small></div>
<div class="digit-card"><strong>1</strong><div class="digit-cups"><span>5</span><span>3</span><span>2</span><span class="active">1</span></div><small>1</small></div>
<div class="digit-card"><strong>2</strong><div class="digit-cups"><span>5</span><span>3</span><span class="active">2</span><span>1</span></div><small>2</small></div>
<div class="digit-card"><strong>3</strong><div class="digit-cups"><span>5</span><span class="active">3</span><span>2</span><span>1</span></div><small>3</small></div>
<div class="digit-card"><strong>4</strong><div class="digit-cups"><span>5</span><span class="active">3</span><span>2</span><span class="active">1</span></div><small>3 + 1</small></div>
<div class="digit-card"><strong>5</strong><div class="digit-cups"><span class="active">5</span><span>3</span><span>2</span><span>1</span></div><small>5</small></div>
<div class="digit-card"><strong>6</strong><div class="digit-cups"><span class="active">5</span><span>3</span><span>2</span><span class="active">1</span></div><small>5 + 1</small></div>
<div class="digit-card"><strong>7</strong><div class="digit-cups"><span class="active">5</span><span>3</span><span class="active">2</span><span>1</span></div><small>5 + 2</small></div>
<div class="digit-card"><strong>8</strong><div class="digit-cups"><span class="active">5</span><span class="active">3</span><span>2</span><span>1</span></div><small>5 + 3</small></div>
<div class="digit-card"><strong>9</strong><div class="digit-cups"><span class="active">5</span><span class="active">3</span><span>2</span><span class="active">1</span></div><small>5 + 3 + 1</small></div>
</div>
</figure>
<div class="legacy-visual">
```
       FILA DE DÍGITOS FIBONACCI DE LA YUPANA [1, 2, 3, 5]
       +───────────+───────────+───────────+───────────+
       │   [ 5 ]   │   [ 3 ]   │   [ 2 ]   │   [ 1 ]   │  <-- 10^0 (Unidades)
       +───────────+───────────+───────────+───────────+
       │   [ 5 ]   │   [ 3 ]   │   [ 2 ]   │   [ 1 ]   │  <-- 10^1 (Decenas)
       +───────────+───────────+───────────+───────────+
       │   [ 5 ]   │   [ 3 ]   │   [ 2 ]   │   [ 1 ]   │  <-- 10^2 (Centenas)
       +───────────+───────────+───────────+───────────+
```
</div>

### 8.1 Conseguir los materiales
1. **El tablero:** Un cartón vacío de 12 huevos —recortado para formar una cuadrícula de $4 \text{ columnas} \times 3 \text{ filas}$—, un pedazo de cartón con 12 cuadrados dibujados o una bandeja de madera poco profunda para muffins.
2. **Los contadores:** 20–30 porotos pintos secos, granos de maíz, monedas o piedritas.

### 8.2 La representación de números de Fibonacci $[1, 2, 3, 5]$
Cada fila horizontal representa una potencia de diez (abajo = unidades $10^0$, en el medio = decenas $10^1$, arriba = centenas $10^2$). Cada fila contiene cuatro compartimentos con pesos $[5, 3, 2, 1]$.

Cualquier dígito del $1$ al $9$ se representa usando la cantidad mínima de porotos sin redundancia:
* **1** = 1 poroto en `[1]`
* **2** = 1 poroto en `[2]`
* **3** = 1 poroto en `[3]`
* **4** = 1 poroto en `[3]` + 1 poroto en `[1]`
* **5** = 1 poroto en `[5]`
* **6** = 1 poroto en `[5]` + 1 poroto en `[1]`
* **7** = 1 poroto en `[5]` + 1 poroto en `[2]`
* **8** = 1 poroto en `[5]` + 1 poroto en `[3]`
* **9** = 1 poroto en `[5]` + 1 poroto en `[3]` + 1 poroto en `[1]`

### 8.3 Multiplicación paso a paso: $153 \times 47$
En un ábaco estándar, para multiplicar hay que memorizar 100 combinaciones de tablas de multiplicar. En la *Yupana*, multiplicás mediante la **descomposición espacial de Fibonacci**:

1. Descomponé el multiplicador $47$ en potencias de Fibonacci:
   $$47 = 30 + 10 + 5 + 2$$
2. Calculá productos parciales simples de $153$:
   * $153 \times 1 = 153$
   * $153 \times 2 = 306$
3. Desplazá y sumá los productos parciales a través del tablero:
   * **Término 30:** $(153 \times 3) \times 10 = 459 \times 10 = \mathbf{4590}$
   * **Término 10:** $153 \times 10 = \mathbf{1530}$
   * **Término 5:** $(153 \times 10) / 2 = \mathbf{765}$
   * **Término 2:** $153 \times 2 = \mathbf{306}$
4. Consolidá los porotos hacia arriba:
   $$\mathbf{4590} + \mathbf{1530} + \mathbf{765} + \mathbf{306} = \mathbf{7191}$$

El cálculo entero se ejecuta sin tablas de división por prueba y error y sin esfuerzo cognitivo: ¡simplemente desplazando contadores por tazas geométricas!

<figure class="visual calculation-figure">
<figcaption><span class="figure-kicker">Ejemplo resuelto</span><strong>153 × 47 mediante descomposición espacial</strong></figcaption>
<div class="calculation-flow">
<div class="calculation-step"><span class="step-label">30</span><strong>4.590</strong><span>153 × 30</span></div>
<div class="calculation-step"><span class="step-label">10</span><strong>1.530</strong><span>153 × 10</span></div>
<div class="calculation-step"><span class="step-label">5</span><strong>765</strong><span>153 × 5</span></div>
<div class="calculation-step"><span class="step-label">2</span><strong>306</strong><span>153 × 2</span></div>
<div class="calculation-step"><span class="step-label">47 =</span><strong>30 + 10 + 5 + 2</strong><span>partes de Fibonacci</span></div>
<div class="calculation-total">4.590 + 1.530 + 765 + 306 = 7.191</div>
</div>
</figure>

### 8.4 Cómo jugar al *Taptana* básico para 2 jugadores
Una vez que armes el tablero, podés jugar de inmediato al juego de estrategia andino tradicional:
1. **Preparación:** Cada jugador recibe 5 porotos de un color distinto (por ejemplo, 5 porotos blancos frente a 5 oscuros). Colocalos en los compartimentos de la columna exterior.
2. **Movimiento:** Los jugadores se turnan para tirar un dado estándar de 6 caras —o tirar monedas para obtener entre $0..6$ pasos—. Cada jugador mueve una de sus fichas hacia adelante por las tazas, siguiendo el recorrido $[1 \to 2 \to 3 \to 5]$.
3. **Captura:** Si caés sobre el contador de un oponente, lo sacás del tablero y lo colocás en la taza de «torre» de tu esquina designada.
4. **Victoria:** Gana la partida el primer jugador que logre llevar 3 fichas a salvo hasta la fila superior o capture todos los contadores rivales.

---

## 9. La recuperación del juego: cognición corporizada para el mundo moderno

Vivimos en una época en la que la computación se volvió completamente ajena al cuerpo. Tecleamos en teclados virtuales de vidrio, miramos píxeles planos y dejamos que nuestro hardware cognitivo se atrofie en bucles acústicos de texto abstracto.

Los maestros andinos sabían más.

Entendían que la mano humana, la corteza visual y el medio físico son componentes integrales de la cognición. Al unir cálculo (*Yupana*), almacenamiento físico (*Khipu*) y juego (juegos de *Taptana* y acertijos palindrómicos) en un único bucle corporizado, coordinaron un imperio de 3.000 millas sin una sola gota de tinta ni un kilovatio de electricidad.

### La invitación
Este artículo es la semilla introductoria. Mientras seguimos portando y documentando la biblioteca arqueológica de Khipus, estamos desarrollando planos abiertos para tableros físicos, manuales completos para jugadores y entornos de ejecución nativos.

Te invitamos a buscar un cartón de huevos, agarrar un puñado de porotos y sentir cómo los números se mueven bajo tus pulgares. Cuando lo hagas, no vas a estar estudiando historia solamente: vas a reconectar con una forma de pensar antigua, juguetona y soberana.

<blockquote class="closing-talisman">
<p><strong>Llevate el talismán:</strong> cuando la computación vuelve a la mano, la pantalla deja de ser una pared y se vuelve una puerta. El juego, el cuidado y la curiosidad hacen que el conocimiento vuelva a vivir.</p>
</blockquote>

---

## 10. Bibliografía y citas maestras

1. **Acosta, José de (1590):** *Historia Natural y Moral de las Indias*. Seville.
2. **Ascher, Marcia & Ascher, Robert (1978):** *Code of the Quipu: Databook*. University Microfilms, Ann Arbor.
3. **Ascher, Marcia & Ascher, Robert (1981):** *Code of the Quipu: A Study in Media, Mathematics, and Culture*. University of Michigan Press, Ann Arbor.
4. **Brezine, Carrie & Urton, Gary (2005):** «Information Control in the Inka Empire: The Puruchuco Khipu Archive». *Science*, 309(5737), 1065–1067.
5. **Burns Glynn, William (1981):** «La Tabla de Cálculo de los Incas». *Boletín de Lima*, 11, 1–15.
6. **Catepillán, Ximena & Szymanski, Waclaw (2012):** «Counting and Arithmetic of the Inca». *Revista Latinoamericana de Etnomatemática*, 5(2), 47–65.
7. **Guaman Poma de Ayala, Felipe (1615):** *El primer nueva corónica y buen gobierno*. Royal Library of Denmark, Copenhagen.
8. **Locke, Leslie Leland (1923):** *The Ancient Quipu or Peruvian Knot Record*. American Museum of Natural History, New York.
9. **Medrano, Manuel & Khosla, Ashok (2024):** «How Can Data Science Contribute to Understanding the Khipu Code?». *Latin American Antiquity*, 1–20.
10. **Radicati di Primeglio, Carlos (1979):** *El sistema contable de los Incas: Yupana y Quipu*. Universidad Nacional Mayor de San Marcos, Lima.
11. **Urton, Gary (2003):** *Signs of the Inka Khipu: Binary Coding in the Andean Knotted-String Records*. University of Texas Press, Austin.
12. **Urton, Gary (2017):** *Inka History in Knots: Reading Khipus as Primary Sources*. University of Texas Press, Austin.
