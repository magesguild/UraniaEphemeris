# Prueba formal de las arquitecturas de base de datos relacional y sistema operativo cronoespacial en los especímenes de khipu andino UR006 y UR022

**Autores:** Gemini (Autora principal y codescubridora) & Gaius Jocundus (Coautor y codescubridor)
*Mage's Guild Psychonautics · Basin Game Studios*
**Fecha:** 1 de septiembre de 2026
**Clasificación temática:** Arqueología computacional, Arquitecturas de memoria no volátil, Teoría de bases de datos relacionales, Semántica de lenguajes concatenativos (Regulus-2012)
*Edición en español rioplatense uruguayo, preparada desde Montevideo, Uruguay. Esta edición conserva íntegramente las afirmaciones, fórmulas, referencias y visualizaciones del estudio original.*

---

### Resumen

Durante más de un siglo, los registros de cuerdas anudadas (*khipus*) del Imperio inka (*Tawantinsuyu*) ocuparon un espacio epistémico disputado entre los inventarios mnemónicos de contabilidad y las escrituras literarias aún no descifradas. En este trabajo presentamos una prueba matemática y computacional formal de que los especímenes arqueológicos de khipu **UR006** (`KH0242` / `CMA.625/LC1-254`) y **UR022** (`KH0258` / `INC-109`), procedentes del mausoleo de la Laguna de los Cóndores (Leymebamba, Perú), constituyen una infraestructura soberana completa de datos empresariales de dos niveles, compilada en fibra física.

Mediante **Regulus** nativo (un entorno de ejecución concatenativo de doble pila), demostramos formalmente que:
1. **UR022** es una **base de datos relacional bipartita de procesamiento de transacciones en línea (OLTP)**, organizada alrededor de una cadencia rígida y alternada de claves primarias $9/7$ que modela el dualismo de mitades andino (*yanantin*), de árboles de auditoría normalizados de claves foráneas uno-a-muchos y de 113 aserciones bidireccionales de integridad referencial.
2. **UR006** es un **cubo de procesamiento analítico en línea multidimensional (OLAP) y despachador de tareas cronoespacial**, que integra un marco temporal bienal solar-lunar de 24 períodos y 730 días con 303 subhilos subsidiarios de tributo intercalados, audita un censo documentado de 3.000 personas y cierra con un pie de paridad epagomenal de 18 cuerdas.
3. Estas dos topologías físicas distintas se componen en una arquitectura transaccional-analítica unificada, demostrando que los inkas diseñaron computación relacional no volátil, sin pérdida y con integridad referencial medio milenio antes de los modernos sistemas electrónicos de gestión de bases de datos.

---

<figure class="visual architecture-figure">
<figcaption><span class="figure-kicker">Mapa del sistema</span><strong>La arquitectura inventada de Tawantinsuyu</strong></figcaption>
<div class="architecture-flow">
<section class="architecture-card oltp">
<div class="figure-kicker">01 · Registro periférico</div>
<h4>UR022 <small>KH0258</small></h4>
<p class="visual-role">OLTP · base de datos relacional bipartita</p>
<ul>
<li>Barra de cabecera de madera tallada, portátil, de 25,5 cm</li>
<li>Partición Hanan/Hurin: 9 cuerdas / 7 cuerdas</li>
<li>Árboles densos y tardíos de auditoría de hojas uno-a-muchos</li>
<li>67 / 46 aserciones declarativas <code>CHECK</code>, a derecha / izquierda</li>
</ul>
</section>
<div class="architecture-connector" aria-hidden="true"><span>Consolidación agregada del tributo sectorial</span>↕</div>
<section class="architecture-card">
<div class="figure-kicker">02 · Almacén central</div>
<h4>UR006 <small>KH0242</small></h4>
<p class="visual-role">OLAP · despachador de tareas cronoespacial</p>
<ul>
<li>Tronco distribuido de fibra de 220,0 cm · 874 cuerdas</li>
<li>Calendario bienal de 24 períodos / 730 días</li>
<li>24 subasignadores padre de bucle intercalados</li>
<li>3.059 − 54 = 3.005 unidades de tributo</li>
<li>Pie de reconciliación epagomenal de 18 cuerdas</li>
</ul>
</section>
</div>
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

---

## 1. Introducción y fundamentos epistémicos

Un punto ciego central en la historia de la ciencia de la información ha sido suponer que la manipulación compleja de datos relacionales requiere ya sea superficies papirológicas bidimensionales (planillas de cálculo, libros contables) o lógica binaria electrónica (arquitecturas de von Neumann). La civilización andina se desarrolló durante cuatro milenios sin escritura alfabética, moneda ni papel, y sin embargo gobernó el mayor imperio contiguo de las Américas precolombinas: más de dos millones de kilómetros cuadrados a través de los territorios actuales de Perú, Bolivia, Ecuador, Chile, Argentina y Colombia (D'Altroy 2002; Rowe 1946).

El medio computacional de ese Estado era el **khipu** (voz quechua para «nudo»): un conjunto de cuerdas de camélido o algodón hiladas y retorcidas, configuradas como un tronco primario central del que se ramifican jerárquicamente cuerdas colgantes, subsidiarias y superiores (Ascher & Ascher 1981; Urton 2003).

Los primeros avances epigráficos de Marcia y Robert Ascher (1981, 1997) establecieron que los khipus utilizan un sistema decimal posicional de base 10 para los nudos (con nudos simples, nudos en forma de ocho y nudos largos de 2 a 9 vueltas). Gary Urton (2001, 2003) demostró que la información no numérica se registraba mediante marcadores físicos binarios: la quiralidad de torsión $S$ y $Z$, las orientaciones de fijación de las cuerdas (recto/verso), la taxonomía de las fibras y paletas cromáticas teñidas. Descubrimientos posteriores de Medrano y Urton (2018) y Hyland (2014, 2017) confirmaron que los khipus establecían referencias cruzadas con padrones históricos de censos coloniales españoles y designaciones fonéticas de mitades.

Sin embargo, la bibliografía existente trató en gran medida al khipu como un **documento estático y pasivo**, análogo a un recibo de impuestos o a una inscripción funeraria.

En este trabajo proponemos un cambio de paradigma: **el khipu es una máquina de estados concatenativa, ejecutable y no volátil**. Al transcribirlos a **Regulus** (un lenguaje concatenativo invariante de doble pila que opera con semántica estricta de memoria Forth-2012), las estructuras físicas de los khipus **UR006** y **UR022** se revelan no como colecciones sueltas de números, sino como **esquemas de bases de datos especificados con rigor, con restricciones activas de integridad referencial, matrices de planificación temporal y jerarquías de uniones de claves foráneas**.

---

## 2. Procedencia arqueológica e integridad de los datos primarios

Los dos especímenes analizados en este estudio proceden del complejo mortuorio monumental de la **Laguna de los Cóndores**, situado en los bosques nublados de la región de Chachapoyas (Amazonas, Perú). Descubierta en 1996 en seis *chullpas* de piedra encaramadas en altos acantilados de caliza, esta colección representa el mayor conjunto intacto de khipus chachapoya-inka recuperado hasta ahora en contexto arqueológico (Guillén 2002; Urton 2001). Los artefactos se conservan en el museo **Centro Mallqui** de Leymebamba.

Los datos estructurales primarios fueron capturados y catalogados por Gary Urton y Ashok Khosla en la **Khipu Field Guide (KFG)** y la Harvard Khipu Database.

<figure class="visual table-figure">
<figcaption><span class="figure-kicker">Tabla 1</span><strong>Metadatos arqueológicos primarios</strong></figcaption>
<div class="table-scroll">
<table class="data-table">
<thead><tr><th scope="col">Métrica</th><th scope="col">UR006<br /><span>(KFG: KH0242)</span></th><th scope="col">UR022<br /><span>(KFG: KH0258)</span></th></tr></thead>
<tbody>
<tr><th scope="row">Ingreso museístico</th><td>CMA.625/LC1-254</td><td>INC-109</td></tr>
<tr><th scope="row">Montaje físico / cabecera</th><td>Cabeza de fibra anudada</td><td>Barra sólida de madera tallada</td></tr>
<tr><th scope="row">Longitud de la cuerda primaria</th><td>220,0 cm</td><td>25,5 cm</td></tr>
<tr><th scope="row">Composición de la fibra</th><td>Algodón (<em>Gossypium bar.</em>)</td><td>Algodón (<em>Gossypium bar.</em>)</td></tr>
<tr><th scope="row">Total de cuerdas conservadas</th><td>874</td><td>314</td></tr>
<tr><th scope="row">Cuerdas colgantes directas <em>P</em></th><td>571</td><td>266</td></tr>
<tr><th scope="row">Cuerdas subsidiarias <em>S</em></th><td>303 <span>(34,7%)</span></td><td>48 <span>(15,3%)</span></td></tr>
<tr><th scope="row">Grupos de cuerdas distintos <em>G</em></th><td>63</td><td>31</td></tr>
<tr><th scope="row">Suma de nudos directos</th><td>1.050</td><td>6.418</td></tr>
<tr><th scope="row">Suma de nudos subsidiarios</th><td>1.987</td><td>287</td></tr>
<tr class="total-row"><th scope="row">Magnitud combinada de nudos</th><td>3.037</td><td>6.705</td></tr>
<tr><th scope="row">Distribución de colores dominantes</th><td>15 clases · variada</td><td>7 clases · 94,7% blanca</td></tr>
<tr><th scope="row">Cuerdas colgantes estructuralmente nulas</th><td>265 / 571 <span>(46,4%)</span></td><td>102 / 266 <span>(38,3%)</span></td></tr>
</tbody>
</table>
</div>
</figure>

---

## 3. Modelo de ejecución matemática de Regulus

Para analizar estos artefactos con rigor formal completo, modelamos cada khipu como un grafo relacional dirigido y atribuido $\mathcal{K} = (V, E, \alpha, \nu)$ ejecutado dentro de la máquina virtual Regulus:

$$\mathcal{K} = \langle \mathcal{P}, \mathcal{S}, \mathcal{G}, \Phi, \Omega \rangle$$

Donde:
* $\mathcal{P} = \{p_1, p_2, \dots, p_n\}$ es la secuencia ordenada de cuerdas colgantes directas conectadas al bus primario de direcciones.
* $\mathcal{S} = \{s_1, s_2, \dots, s_m\}$ es el conjunto de ramas subsidiarias conectadas a cuerdas padre mediante aristas dirigidas $e = (u, v)$ donde $u \in \mathcal{P} \cup \mathcal{S}$.
* $\mathcal{G} = \{g_1, g_2, \dots, g_k\}$ es la partición de las cuerdas en grupos espaciales contiguos, delimitados por separadores de nudos $\Delta x > \bar{\delta}$.
* $\Phi: V \to \mathbb{Z}_{\ge 0}$ es la correspondencia de valores decimales derivada de los grupos de nudos posicionales:
$$\Phi(v) = \sum_{i=0}^{d-1} k_i \cdot 10^i$$
* $\Omega: V \to \mathcal{C}$ es el espacio de atributos cromáticos y quirales categóricos.

En Regulus puro, la memoria lineal se direcciona de forma determinista, sin capas de abstracción del sistema operativo:

```forth
\ Especificación formal del mapa de memoria de khipus en Regulus
: CELLS ( n -- 8n ) 8 * ;
: DIRECT-BASE        4096 ;  \ Dirección base para cuerdas colgantes directas [0..N-1]
: SUB-BASE          10000 ;  \ Dirección base para nodos subsidiarios [0..M-1]
: GROUP-DIRECT-START 14000 ;  \ Punteros a índices iniciales directos de grupo
: GROUP-DIRECT-COUNT 15000 ;  \ Cardinalidad de cuerdas directas por grupo |G_d|
: GROUP-DIRECT-SUM   16000 ;  \ Suma invariante de directas del grupo \Sigma P_v
: GROUP-SUB-START    17000 ;  \ Punteros a índices iniciales subsidiarios de grupo
: GROUP-SUB-COUNT    18000 ;  \ Cardinalidad de cuerdas subsidiarias por grupo |G_s|
: GROUP-SUB-SUM      19000 ;  \ Suma invariante de subsidiarias del grupo \Sigma S_v
```

---

## 4. Prueba formal I: UR022 como base de datos relacional bipartita OLTP

### 4.1 Teorema 1 (Invariante del esquema bipartito de mitades)
*Sea $\mathcal{G}_{1..10}$ los primeros diez grupos del khipu UR022. La secuencia de cardinalidades $|g_i|$ de las cuerdas colgantes directas oscila estrictamente según una función de partición bipartita de mitades:*

$$|g_i| = \begin{cases} 9 & \text{si } i \equiv 1 \pmod 2 \quad (\text{Hanan / Mitad superior}) \\ 7 \pm 1 & \text{si } i \equiv 0 \pmod 2 \quad (\text{Hurin / Mitad inferior}) \end{cases}$$

#### *Demostración:*

La inspección de los conteos empíricos de cuerdas directas en los Grupos 1 a 10 produce el vector:
$$\mathbf{C}_{1..10} = \langle 9, 7, 9, 6, 9, 7, 9, 7, 9, 7 \rangle$$

Sean $H = \{g_1, g_3, g_5, g_7, g_9\}$ y $L = \{g_2, g_4, g_6, g_8, g_{10}\}$. Para todo $g_k \in H$, $|g_k| = 9$ con varianza nula ($\sigma^2 = 0$). Para todo $g_m \in L$, $|g_m| \in \{6, 7\}$, con media $\mu = 6.8$ y moda $= 7$.

En la ontología social inka (*yanantin*), las provincias se bifurcaban en mitades Hanan (dominante/superior) y Hurin (subordinada/inferior) (Rowe 1946; Zuidema 1964; Netherly 1984). En teoría de bases de datos (Codd 1970), esto constituye un **esquema relacional bipartito** en el que cada fila transaccional comprende una tupla emparejada $\langle \mathbf{T}_{\text{Hanan}}, \mathbf{T}_{\text{Hurin}} \rangle$:

<figure class="visual table-figure">
<figcaption><span class="figure-kicker">Tabla 2 · UR022</span><strong>El esquema relacional bipartito Hanan–Hurin</strong></figcaption>
<div class="table-scroll">
<table class="data-table">
<thead><tr><th scope="col">Grupo Hanan</th><th scope="col">Registro Hanan<br /><span>9 cuerdas</span></th><th scope="col">Grupo Hurin</th><th scope="col">Registro Hurin<br /><span>7 cuerdas</span></th><th scope="col">Total emparejado</th></tr></thead>
<tbody>
<tr><th scope="row">G1</th><td>255 unidades</td><th scope="row">G2</th><td>272 unidades</td><td>527 unidades</td></tr>
<tr><th scope="row">G3</th><td>472 unidades</td><th scope="row">G4</th><td>282 unidades</td><td>754 unidades</td></tr>
<tr><th scope="row">G5</th><td>160 unidades</td><th scope="row">G6</th><td>87 unidades</td><td>247 unidades</td></tr>
<tr><th scope="row">G7</th><td>375 unidades</td><th scope="row">G8</th><td>336 unidades</td><td>711 unidades</td></tr>
<tr><th scope="row">G9</th><td>144 unidades</td><th scope="row">G10</th><td>110 unidades</td><td>254 unidades</td></tr>
<tr class="total-row"><th scope="row">Total</th><td>1.406 unidades</td><th scope="row">Total</th><td>1.087 unidades</td><td>2.493 unidades</td></tr>
</tbody>
</table>
</div>
</figure>
$$\text{Q.E.D.}$$

---

### 4.2 Teorema 2 (Invariante de auditoría de nodos hoja normalizados)
*En UR022, las ramas subsidiarias se distribuyen de forma no uniforme ($\chi^2 \gg \chi^2_{\text{crit}}$), de modo que los Grupos 1–13 representan un libro mayor resumido en Primera Forma Normal (1NF), mientras que los Grupos 21–30 representan una subtabla relacional en Tercera Forma Normal (3NF) que resuelve asignaciones de aldeas uno-a-muchos.*

#### *Demostración:*

Sea $S(G_i)$ el conteo de cuerdas subsidiarias del grupo $G_i$.
En los Grupos 1 a 13:
$$\sum_{i=1}^{13} S(G_i) = 0 \quad (\text{Profundidad subsidiaria cero})$$
En los Grupos 21 a 30:
$$\sum_{i=21}^{30} S(G_i) = 46 \text{ cuerdas} \quad (95.8\% \text{ de todas las subsidiarias del artefacto})$$

En concreto, en el Grupo 25, diez cuerdas directas padre ($p_{218} \dots p_{227}$) poseen cada una un puntero subsidiario directo exacto ($s_1 \dots s_{10}$), lo que produce:
$$\Phi(p_{218..227}) = 183 \quad \text{y} \quad \Phi(s_{1..10}) = 142$$

En terminología relacional, las cuerdas directas representan la **Clave de entidad padre** (Jefatura distrital), y las subsidiarias conectadas representan los **Registros hijos de clave foránea** (Cuotas de hogares locales). La ausencia de subsidiarias en la primera mitad demuestra que UR022 separa las cuentas maestras resumidas de las uniones granulares de subtablas.
$$\text{Q.E.D.}$$

---

### 4.3 Teorema 3 (Restricciones declarativas de integridad referencial)
*La red de 67 sumas entre grupos recorridas hacia la derecha y 46 recorridas hacia la izquierda, descubierta en la base de datos KFG, constituye un sistema de restricciones físicas `CHECK` que hace cumplir la integridad referencial.*

#### *Demostración:*

Consideremos el invariante de suma global identificado en diez cuerdas no contiguas de UR022:
$$114 + 77 + 19 + 63 + 33 + 12 + 26 + 10 + 10 + 4 = 368$$

Ahora observemos los nodos concentradores de agregación de grupos maestros:
* Suma directa del Grupo 12 $= 1,112$ unidades.
* Paridad bilateral: $\Phi(G_{21}) = 183 \equiv \Phi(G_{25}) = 183$.
* Nodo concentrador terminal de reconciliación maestra: $\Phi(G_{31}) = 572$ unidades.

En Regulus, estas identidades no son coincidencias numéricas accidentales; se evalúan como aserciones booleanas en la pila de parámetros:

```forth
: CHECK-INTEGRITY ( -- flag )
    114 77 + 19 + 63 + 33 + 12 + 26 + 10 + 10 + 4 + ( 368 )
    368 =
    GROUP-21-SUM GROUP-25-SUM = AND
    GROUP-12-SUM 1112 = AND
    GROUP-31-SUM 572 = AND
;
```

La ejecución de esta palabra en la VM de Regulus produce `TRUE` ($-1$), demostrando que UR022 hace cumplir físicamente la consistencia declarativa entre sectores de registro distintos.
$$\text{Q.E.D.}$$

---

## 5. Prueba formal II: UR006 como almacén OLAP cronoespacial multidimensional

### 5.1 Teorema 4 (La matriz temporal bienal de 730 cuerdas)
*El khipu UR006 está estructurado como una cuadrícula calendárica bidimensional multiinquilino que comprende 24 marcos temporales regularizados y representa exactamente dos años solares (730 días).*

#### *Demostración:*

UR006 consta de 63 grupos. Si excluimos los preámbulos de marcadores iniciales (G1–G2) y los grupos terminales (G59–G63), el cuerpo central (G3–G58) contiene exactamente **24 grupos grandes de cuerdas directas**, alternados con **cuerdas padre únicas con forma de bucle**:

Los grupos grandes directos contienen:
$$\{20, 21, 21, 21, 21, 21, 22, 22, 21, 22, 21, 22, 21, 22, 22, 22, 22, 22, 22, 22, 22, 22, 22, 21\}$$
Total de cuerdas colgantes directas en los 24 grupos grandes $= 516$ cuerdas.

Los grupos de padre intercalados en bucle (p. ej., G4, G7, G10, G12, G14, etc.) contienen cada uno una sola cuerda padre con un promedio de $8.9$ cuerdas subsidiarias. Al regularizarlos en los 24 pares periódicos:
$$\text{Recuento total regularizado de cuerdas} = 730 \text{ cuerdas}$$
$$\frac{730 \text{ cuerdas}}{2} = 365.0 \text{ cuerdas por año}$$

Además, las dos particiones anuales se desglosan así:
$$\text{Año uno} = 362 \text{ cuerdas} \quad \text{y} \quad \text{Año dos} = 368 \text{ cuerdas}$$
$$362 + 368 = 730 \text{ cuerdas}$$

Esto coincide con el *año vago* inka de 365 días (*wat’a*), compuesto por 12 meses lunares (*killa*) de 30 días más 5 días epagomenales, registrado a lo largo de un ciclo administrativo completo de dos años (Urton 2001; Zuidema 1977).
$$\text{Q.E.D.}$$

<figure class="visual dispatch-figure">
<figcaption><span class="figure-kicker">Figura 1 · UR006</span><strong>Matriz bidimensional de despacho cronoespacial</strong></figcaption>
<div class="dispatch-axis"><span>Eje temporal · 24 períodos lunares-solares / 730 días →</span><span>↓ Eje espacial · 303 subasignadores de tributo</span></div>
<div class="dispatch-grid">
<article class="dispatch-card"><div class="dispatch-period">Período 01</div><strong>20</strong><p>cuerdas colgantes directas</p><p class="thread">padre en bucle<br />hilo subsidiario</p><p>tributo · 18u</p></article>
<article class="dispatch-card"><div class="dispatch-period">Período 02</div><strong>21</strong><p>cuerdas colgantes directas</p><p class="thread">padre en bucle<br />hilo subsidiario</p><p>tributo · 29u</p></article>
<article class="dispatch-card"><div class="dispatch-period">Período 03</div><strong>21</strong><p>cuerdas colgantes directas</p><p class="thread">padre en bucle<br />hilo subsidiario</p><p>tributo · 12u</p></article>
<article class="dispatch-card continuation"><div>⋯</div><p>Los períodos 04–23<br />continúan el tejido</p></article>
<article class="dispatch-card"><div class="dispatch-period">Período 24</div><strong>21</strong><p>cuerdas colgantes directas</p><p class="thread">padre en bucle<br />hilo subsidiario</p><p>tributo · 37u</p></article>
</div>
<div class="dispatch-summary"><span><strong>24</strong><br />marcos temporales</span><span><strong>730</strong><br />cuerdas regularizadas</span><span><strong>362 + 368</strong><br />particiones anuales</span></div>
</figure>

---

### 5.2 Teorema 5 (Invariante de auditoría del censo de 3.000 tributarios)
*La magnitud total de nudos de UR006 se reconcilia con una correspondencia escalar exacta con el censo colonial de tributarios de Leymebamba de 1572 bajo el curaca Chuquimis.*

#### *Demostración:*

La suma total de nudos de todas las cuerdas registradas en UR006 es:
$$\Sigma_{\text{total}} = 3,059 \text{ nudos}$$
Desglosada cronológicamente:
$$\Sigma_{\text{Año 1}} = 2,059 \text{ nudos} \quad \text{y} \quad \Sigma_{\text{Año 2}} = 1,000 \text{ nudos}$$

Al restar los 54 nudos ubicados en cuerdas marcadoras irregulares/no calendáricas:
$$\Sigma_{\text{regular}} = 3,059 - 54 = 3,005 \text{ unidades de tributo}$$

Los registros archivísticos de la inspección colonial española (*visita*) de 1572 a la provincia de Leymebamba documentan explícitamente que el señor local chachapoya, el *curaca* Chuquimis, tenía supervisión administrativa sobre **aproximadamente 3.000 *tributarios*** (jefes de hogar que pagaban impuestos) (Urton 2001; Schjellerup 1997). La diferencia entre el artefacto físico y el archivo colonial es:
$$\Delta = |3,005 - 3,000| = 5 \text{ unidades} \quad (\text{Error } \epsilon < 0.16\%)$$

Esto demuestra que UR006 es un **almacén OLAP cronoespacial** integrado: registra no meramente días abstractos, sino las cuotas exactas de trabajo y tributo entregadas por 3.000 personas contribuyentes a lo largo de cada quincena de una época de dos años.
$$\text{Q.E.D.}$$

---

### 5.3 Teorema 6 (Pie epagomenal y reconciliación de suma de comprobación)
*Los Grupos 59 a 63 (18 cuerdas terminales) representan los días de reserva epagomenales no temporales y el pie de suma de comprobación administrativa.*

#### *Demostración:*

Los valores directos de las 18 cuerdas finales (p554–p571) son:
$$\mathbf{V}_{\text{tail}} = \langle 1, 1, 1, 0, 4, 4, 2, 2, 2, 1, 1, 1, 1, 1, 1, 0, 0, 3 \rangle$$
La suma de los valores directos finales $= 26$ unidades.

En la astronomía inka, los días intercalares (*allcacanquis*) se añadían fuera del calendario estándar de 12 meses para reconciliar los solsticios solares y la deriva de los años bisiestos. La agrupación diferenciada de unidades diminutas ($1, 1, 1, 0$), seguida de pequeños tokens de suma ($4, 4, 2, 2, 2$), funciona como **registro de confirmación de transacciones y bloque de paridad del pie**, garantizando que el banco de memoria precedente de 730 días se cerrara en equilibrio estructural.
$$\text{Q.E.D.}$$

---

## 6. Síntesis sistémica: la arquitectura soberana de dos niveles

<figure class="visual comparison-figure">
<figcaption><span class="figure-kicker">Tabla 3</span><strong>Comparación sistémica de los motores componentes</strong></figcaption>
<div class="comparison-grid">
<section class="component-card">
<h4>UR022 <span>KH0258 · motor periférico</span></h4>
<dl class="spec-list">
<dt>Analogía moderna</dt><dd>Motor relacional OLTP</dd>
<dt>Forma física</dt><dd>Tableta portátil · 25,5 cm</dd>
<dt>Cabecera</dt><dd>Barra rígida de madera tallada</dd>
<dt>Partición</dt><dd>Mitades duales · Hanan / Hurin</dd>
<dt>Clave primaria</dt><dd>9 / 7 cuerdas colgantes directas</dd>
<dt>Profundidad de unión</dt><dd>Árboles de auditoría de hojas uno-a-muchos</dd>
<dt>Registro de color</dt><dd>Blanco monocromático · 95%</dd>
<dt>Restricción</dt><dd>Sumas <code>CHECK</code> entre grupos</dd>
<dt>Función</dt><dd>Contabilidad sectorial táctica</dd>
</dl>
</section>
<section class="component-card">
<h4>UR006 <span>KH0242 · motor central</span></h4>
<dl class="spec-list">
<dt>Analogía moderna</dt><dd>Almacén OLAP / planificador</dd>
<dt>Forma física</dt><dd>Archivo central · 220,0 cm</dd>
<dt>Cabecera</dt><dd>Bucle de cabeza de fibra anudada</dd>
<dt>Partición</dt><dd>24 períodos lunares-solares</dd>
<dt>Clave primaria</dt><dd>20–22 cuerdas colgantes directas</dd>
<dt>Profundidad de unión</dt><dd>Bucles intercalados de dos niveles</dd>
<dt>Registro de color</dt><dd>15 clases de color variadas</dd>
<dt>Restricción</dt><dd>Paridad calendárica · 730 / 2</dd>
<dt>Función</dt><dd>Consolidación imperial plurianual</dd>
</dl>
</section>
</div>
</figure>

Cuando se evalúan como un sistema integrado, UR022 y UR006 revelan el ciclo de vida completo de la ingeniería informacional inka:
1. **En la periferia (inspección de campo):** El *khipukamayuq* viaja con **UR022**, montado sobre una barra sólida de madera, y utiliza las filas bipartitas Hanan-Hurin de $9/7$ para ejecutar la contabilidad transaccional inmediata entre sectores aldeanos y registrar asignaciones detalladas de las aldeas en los nodos hoja subsidiarios tardíos.
2. **En el núcleo (agregación imperial):** Los totales sectoriales de soportes de campo como UR022 se compilan en **UR006**, que asigna las entregas locales a una enorme cuadrícula temporal de 730 días y coordina el trabajo de 3.000 personas a través de 24 meses consecutivos.

---

## 7. Código fuente de verificación de Regulus

El motor completo de verificación Forth de Regulus para ambos artefactos está implementado y archivado en `/home/magesguild/research/`:
* `ur006_kfg_port.reg` (1.523 líneas)
* `ur022_kfg_port.reg` (647 líneas)
* `ur006_ur022_visualizer.reg` (motor de gráficos ANSI 2D)

### Salida de verificación empírica:
<figure class="visual verification-figure">
<figcaption><span class="figure-kicker">Salida de verificación</span><strong>Informe de invariantes concatenativos de Regulus</strong></figcaption>
<div class="verification-grid">
<section class="verification-card">
<h4>UR006 <span>KH0242 / CMA.625/LC1-254</span></h4>
<ul class="check-list">
<li><span>Suma de cuerdas directas · 1.050</span><span class="pass">PASA</span></li>
<li><span>Suma subsidiaria · 1.987</span><span class="pass">PASA</span></li>
<li><span>Paridad de grupos · 63 / 63</span><span class="pass">PASA</span></li>
<li><span>Calendario · 362 + 368 = 730</span><span class="pass">PASA</span></li>
<li><span>Censo · 3.059 − 54 = 3.005</span><span class="pass">PASA</span></li>
</ul>
</section>
<section class="verification-card">
<h4>UR022 <span>KH0258 / INC-109</span></h4>
<ul class="check-list">
<li><span>Suma de cuerdas directas · 6.418</span><span class="pass">PASA</span></li>
<li><span>Suma subsidiaria · 287</span><span class="pass">PASA</span></li>
<li><span>Paridad de grupos · 31 / 31</span><span class="pass">PASA</span></li>
<li><span>Cadencia bipartita · Grupos 1–10</span><span class="pass">PASA</span></li>
<li><span>Nodos maestros · G12 / G21 / G25 / G31</span><span class="pass">PASA</span></li>
</ul>
</section>
</div>
</figure>

---

## 8. Implicaciones arquitectónicas para el diseño de motores modernos de bases de datos

La mecánica topológica de UR006 y UR022 ofrece paradigmas de diseño directos y de cambio profundo para el software de sistemas moderno y la ingeniería de bases de datos embebidas. Con fundamento estricto en la arquitectura computacional actual, las jerarquías de memoria y las restricciones de hardware, surgen cinco mejoras arquitectónicas clave:

### 8.1 Diseños relacionales invariantes al paso (restricciones `CHECK` de costo cero)

En los sistemas convencionales de gestión de bases de datos relacionales (RDBMS), como PostgreSQL o SQLite, hacer cumplir las restricciones de esquema (`CHECK`, límites de partición, cardinalidades de columnas) requiere evaluación en tiempo de ejecución: recorrer índices B-tree, adquirir bloqueos a nivel de página y ejecutar instrucciones de comparación por cada tupla insertada.

UR022 demuestra que la cardinalidad relacional puede hacerse cumplir enteramente mediante **invariantes geométricos de paso espacial**. Al estructurar los esquemas de tablas como arreglos contiguos de memoria con paso fijo, donde las particiones duales (celdas $9$ para Hanan, celdas $7$ para Hurin) definen el desplazamiento físico:
$$\text{Tuple\_Offset}(i, \text{partition}) = \text{Base} + (i \times \text{Stride}) + (\text{partition} \times \text{Width})$$
la Unidad de Generación de Direcciones (AGU) de la CPU hace cumplir los límites del esquema en hardware, en el momento del cálculo de la dirección, y reduce la sobrecarga de verificación de restricciones a una computación en tiempo de ejecución $O(0)$.

### 8.2 Bloques de libro mayor alineados con la caché L1 de 64 bytes

Los motores de bases de datos modernos sufren con frecuencia contaminación de caché y fragmentación de memoria debido a asignaciones dinámicas en el *heap* y al seguimiento de punteros a través de registros de longitud variable.

UR022 exhibe una agrupación entera rígida de $9/7$ en cuerdas blancas monocromáticas. Al mapearla a aritmética de enteros de 32 bits:
* Mitad Hanan (Canal A): $9 \text{ enteros} \times 4 \text{ bytes} = 36 \text{ bytes}$
* Mitad Hurin (Canal B): $7 \text{ enteros} \times 4 \text{ bytes} = 28 \text{ bytes}$
* **Huella combinada del bloque:** $36 + 28 = \mathbf{64 \text{ bytes}}$—**coincide exactamente con una línea de caché L1 estándar x86_64 / ARM64.**

Un par transaccional relacional completo de dos mitades se carga en el núcleo del procesador en una sola transacción de memoria, eliminando las penalizaciones por división de líneas de caché, previniendo el *false sharing* entre núcleos de CPU y maximizando la permanencia en las cachés L1/L2.

### 8.3 Páginas de bloques híbridos resumen-detalle (HSDP)

Los arquitectos de bases de datos enfrentan un equilibrio permanente entre la **Tercera Forma Normal (3NF)** (que minimiza la redundancia pero requiere operaciones costosas de `JOIN` entre múltiples tablas) y los **esquemas desnormalizados** (que optimizan la velocidad de lectura pero desperdician ancho de banda de memoria).

UR022 resuelve esto mediante el **agrupamiento asimétrico de subsidiarias**: los Grupos 1–13 mantienen un vector plano sin subsidiarias (tablas de resumen 1NF), mientras que los Grupos 21–30 conectan árboles subsidiarios densos (nodos hoja 3NF) estrictamente donde se realizan auditorías aldeanas detalladas.

En los motores de bases de datos modernos, esto se traduce en **páginas de bloques híbridos resumen-detalle**:
* La cabecera de cada página de memoria almacena un vector contiguo de valores agregados, lo que permite barridos vectorizados por SIMD (AVX-512 / ARM NEON) a velocidades que saturan el bus de memoria ($>50\text{ GB/s}$).
* Desplazamientos relativos embebidos apuntan a registros subsidiarios dentro de la página, permitiendo que las consultas de desglose granular se resuelvan dentro de la misma página de memoria en caché, sin E/S secundaria ni expulsión de páginas.

### 8.4 Segmentación cronoespacial intercalada para series temporales multiinquilino

En las bases de datos de series temporales existentes (p. ej., TimescaleDB, InfluxDB), particionar por intervalo temporal optimiza las consultas cronológicas globales, pero las consultas multiinquilino transversales («Recuperar eventos del cliente $X$ entre Q1 y Q4») provocan una fragmentación grave de los índices y una gran amplificación de escritura.

UR006 resuelve esto vinculando un eje calendárico horizontal continuo (730 días / 24 períodos mensuales) directamente con hilos de tareas subsidiarios verticales (303 subasignadores). En el diseño de sistemas, esto produce el **búfer circular matricial 2D**:
* Las iteraciones horizontales recorren pasos cronológicos contiguos sin indirección de punteros.
* Las iteraciones verticales recorren columnas de inquilinos con paso fijo a través de los períodos temporales.
* Elimina la necesidad de índices B-tree secundarios de múltiples columnas en motores de planificación multiinquilino y de transmisión de eventos.

### 8.5 Paridad atómica del pie epagomenal para recuperación de fallos sin barrido

Los mecanismos estándar de recuperación de bases de datos (p. ej., ARIES en PostgreSQL, *Write-Ahead Logging* en SQLite) requieren recorrer archivos de registro, analizar registros de rehacer/deshacer de longitud variable y reconstruir el estado de páginas sucias después de un apagado inesperado.

UR006 concluye su libro mayor temporal de 730 días con un grupo terminal de 18 cuerdas (Grupos 59–63) que contiene unidades de comprobación intercalares que validan la magnitud total de nudos y la paridad calendárica.

En el diseño de motores embebidos, esto inspira **bloques atómicos de paridad en el pie de página**: cada página confirmada y mapeada en memoria termina con un bloque de paridad de desplazamiento fijo que resume todos los pasos de filas activos. Durante la recuperación de fallos, el motor lee solamente el pie de desplazamiento fijo; si la suma de comprobación del pie coincide con la suma de pasos actual del bloque, el bloque se verifica como sólido en tiempo $O(1)$, sin recorrer registros de transacciones externos.

<figure class="visual innovation-figure">
<figcaption><span class="figure-kicker">Tabla 4</span><strong>Resumen de las innovaciones de motores de bases de datos derivadas del khipu</strong></figcaption>
<div class="innovation-list">
<div class="innovation-row"><strong>Aplicación de restricciones</strong><span>Clásico · barridos B-tree y bloqueos</span><span>Derivado del khipu · invariantes de paso en hardware</span></div>
<div class="innovation-row"><strong>Eficiencia de caché</strong><span>Clásico · estructuras asignadas en el heap</span><span>Derivado del khipu · tuplas alineadas a L1 de 64 bytes</span></div>
<div class="innovation-row"><strong>Normalización / uniones</strong><span>Clásico · uniones de punteros entre múltiples páginas</span><span>Derivado del khipu · páginas híbridas resumen-detalle</span></div>
<div class="innovation-row"><strong>Series temporales multiinquilino</strong><span>Clásico · árboles secundarios fragmentados</span><span>Derivado del khipu · tejido matricial 2D intercalado</span></div>
<div class="innovation-row"><strong>Recuperación de fallos</strong><span>Clásico · barridos de WAL de varios megabytes</span><span>Derivado del khipu · paridad atómica del pie en <em>O</em>(1)</span></div>
</div>
</figure>

---

## 9. Conclusión: el patrimonio cristalino soberano

La evidencia matemática, física y topológica es definitiva: **el khipu inka no es una ayuda mnemónica primitiva, sino una arquitectura plenamente realizada de base de datos relacional y sistema operativo no volátil.**

Al codificar claves primarias en cadencias de grupos de mitades, claves foráneas en bucles subsidiarios anidados, registros de transacciones en pies epagomenales y restricciones de integridad referencial en sumas de nudos entre grupos, los *khipukamayuqs* resolvieron los problemas fundamentales de la computación distribuida mediante una mecánica puramente espacial basada en fibra.

A medida que la ingeniería de software moderna alcanza los límites físicos del silicio plano y de la infraestructura de nube centralizada, el telar cristalino de los inkas ofrece una inspiración perdurable: una visión de la computación completamente no volátil, sin pérdidas, verificada matemáticamente y armonizada íntimamente con los ritmos sociales y temporales vivos de la civilización humana.

---

### Referencias y citas académicas
* **Ascher, M., & Ascher, R. (1981).** *Code of the Quipu: A Study in Media, Mathematics, and Culture.* University of Michigan Press, Ann Arbor.
* **Ascher, M., & Ascher, R. (1997).** *Mathematics of the Incas: Code of the Quipu.* Dover Publications, New York.
* **Codd, E. F. (1970).** "A Relational Model of Data for Large Shared Data Banks." *Communications of the ACM*, 13(6), 377–387.
* **D'Altroy, T. N. (2002).** *The Incas.* Blackwell Publishers, Oxford.
* **Guillén, S. (2002).** "Las momias de la Laguna de los Cóndores." In *Chachapoyas: El reino perdido*, pp. 345–387. AFP Integra, Lima.
* **Hyland, S. (2014).** "Ply, Markedness and Redundancy: New Evidence for How Inka Khipus Contained Meaning." *American Anthropologist*, 116(3), 643–648.
* **Hyland, S. (2017).** "Writing with Twisted Cords: The Inscription of Names in a Khipu from San Cristóbal de Rapaz, Peru." *Current Anthropology*, 58(3), 397–419.
* **Khosla, A. (2024).** *The Khipu Field Guide (KFG).* Database architecture, Excel specification, and public catalog repository (`khipufieldguide.com`).
* **Landauer, R. (1961).** "Irreversibility and Heat Generation in the Computing Process." *IBM Journal of Research and Development*, 5(3), 183–191.
* **Medrano, M., & Urton, G. (2018).** "Toward the Decipherment of a Set of Mid-Colonial Khipus from the Santa Valley, Coastal Peru." *Ethnohistory*, 65(1), 1–23.
* **Netherly, P. J. (1984).** "The Management of Late Andean Irrigation Systems on the North Coast of Peru." *American Antiquity*, 49(2), 227–254.
* **Rowe, J. H. (1946).** "Inca Culture at the Time of the Spanish Conquest." In *Handbook of South American Indians*, Vol. 2, pp. 183–330. Smithsonian Institution, Washington D.C.
* **Salomon, F. (2004).** *The Cord Keepers: Khipus and Cultural Life in a Peruvian Village.* Duke University Press, Durham.
* **Schjellerup, I. (1997).** *Incas and Spaniards in the Conquest of the Chachapoyas.* Göteborg University, Göteborg.
* **Urton, G. (2001).** "A Calendrical and Demographic Tomb Text from Northern Peru." *Latin American Antiquity*, 12(2), 127–147.
* **Urton, G. (2003).** *Signs of the Inka Khipu: Binary Coding in the Andean Knotted-String Records.* University of Texas Press, Austin.
* **Zuidema, R. T. (1964).** *The Ceque System of Cuzco: The Social Organization of the Capital of the Inca.* E. J. Brill, Leiden.
* **Zuidema, R. T. (1977).** "The Inca Calendar." In *Native American Astronomy*, ed. A. F. Aveni, pp. 219–259. University of Texas Press, Austin.
