# **Manual de Campo para Educadores: El Sistema Arcade Khipu Inca e Informática Somática**

**Guía Pedagógica Completa para la Aritmética Andina Táctil**

*Basin Game Studios / Mage's Guild Psychonautics (c) 2026*

*MIT LICENSE - LIBRE*

## 1. Resumen Ejecutivo y Fundamentos Pedagógicos

### Objetivo

Enseñar a los estudiantes aritmética decimal posicional, descomposición
matricial espacial y lógica digital sin pérdidas, sin depender de la
memorización abstracta, pilas de datos externas ni cálculos
electrónicos.

### Filosofía Central: Computación Somática y Espacio de Fases Discreto

La **Yupana** (tablero de conteo incaico) y el **Khipu** (archivo de
cuerdas con nudos) forman una arquitectura unificada de procesamiento
táctil de información:

- **La Yupana es la ALU / Memoria RAM:** Un tablero físico y dinámico
  donde los cálculos se realizan en tiempo real moviendo fichas (granos
  de quinua, maíz o piedras) directamente dentro de los receptáculos o
  vasijas.

- **El Khipu es el Almacenamiento de Software No Volátil:** Un registro
  físico permanente donde los estados finales de la Yupana se guardan en
  redes de cuerdas mediante métricas de nudos posicionales.

- **Ejecución por Pasos de Reloj (Espacio de Fases):** En lugar de
  realizar cálculos mentales rígidos por cada grano individual, el
  operador usa sus manos para instanciar estados físicos colocando
  múltiples granos en las vasijas. En un "paso de reloj" elegido (un
  barrido manual deliberado a través del tablero), el operador aplica
  reglas locales simples (fusiones, avalanchas, destejidos) para
  permitir que el sistema se "asiente" en su camino de menor
  resistencia, su atractor gravitacional natural.

### Objetivos de Aprendizaje

Al completar este módulo, los estudiantes podrán:

1.  Representar cualquier número decimal del 0…9.999 en una cuadrícula
    geométrica de 4 vasijas utilizando no más de 3 fichas físicas por
    fila.

2.  Realizar sumas y restas mediante "fusiones", "avalanchas" y
    "destejidos" fluidos en lugar de algoritmos memorizados de acarreo o
    préstamo.

3.  Ejecutar multiplicaciones y divisiones de varios dígitos
    completamente en el tablero mediante desplazamientos espaciales y
    asignación equitativa (*Ayni*).

4.  Comprender cómo los sistemas táctiles no basados en silicio procesan
    cargas de trabajo computacionales complejas de forma determinista.

## 2. Materiales y Configuración Física

### Materiales Requeridos (Por Estudiante o Pareja)

1.  **1 × Tablero Yupana:** Una cuadrícula de 5 filas por 4 columnas
    geométricas.

    - *Alternativas de Aula:* Cartones de huevos (una cuadrícula de 5×4
      huecos) o cuadrículas dibujadas en papel/pizarra.

2.  **30–40 Fichas Físicas:** Granos de quinua, maíz seco, piedras
    pequeñas o fichas de plástico. *(¡No se requieren tarjetas, pilas de
    papel ni rastreadores de estado externos!)*

### Topología del Tablero

| **NIVEL / FILA**      | **\[5\]** | **\[3\]** | **\[2\]** | **\[1\]** | **VALOR DEL NIVEL**           |
|-----------------------|-----------|-----------|-----------|-----------|-------------------------------|
| $10^{4}$ **(10.000)** | ( )       | ( )       | ( )       | ( )       | = 0                           |
| $10^{3}$ **(1.000)**  | ( )       | ( )       | ( )       | ( )       | = 0                           |
| $10^{2}$ **(100)**    | (●)       | ( )       | (●)       | ( )       | = **700** *\[(5 + 2) × 100\]* |
| $10^{1}$ **(10)**     | ( )       | (●)       | ( )       | (●)       | = **40** *\[(3 + 1) × 10\]*   |
| $10^{0}$ **(1)**      | (●)       | (●)       | ( )       | (●)       | = **9** *\[(5 + 3 + 1) × 1\]* |

- **Eje Vertical (Potencias de 10):** La fila inferior corresponde a las
  Unidades ($10^{0}$), subiendo a Decenas ($10^{1}$), Centenas
  ($10^{2}$), Unidades de Millar ($10^{3}$) y Decenas de Millar
  ($10^{4}$).

- **Eje Horizontal (Las 4 Vasijas Mágicas):** Cada fila contiene cuatro
  receptáculos físicos con valores de **\[5\]**, **\[3\]**, **\[2\]** y
  **\[1\]**.

## 3. Unidad 1: Representación de Dígitos y la Regla de Oro

### Concepto de la Lección

Cualquier dígito decimal (0…9) se forma en una sola fila sumando los
valores de las vasijas que contienen granos.

**La Regla de Oro:** Coloca siempre los granos en la vasija disponible
de mayor valor que quepa dentro del resto del número.

Esta regla garantiza que **ningún dígito requiera jamás más de 3
granos** cuando el tablero está en estado de reposo.

### Tabla de Referencia de Codificación para Educadores

| **Dígito** | **Combinación de Vasijas** | **Total de Granos** |
|------------|----------------------------|---------------------|
| **0**      | Fila Vacía                 | 0                   |
| **1**      | \[1\]                      | 1                   |
| **2**      | \[2\]                      | 1                   |
| **3**      | \[3\]                      | 1                   |
| **4**      | \[3\] + \[1\]              | 2                   |
| **5**      | \[5\]                      | 1                   |
| **6**      | \[5\] + \[1\]              | 2                   |
| **7**      | \[5\] + \[2\]              | 2                   |
| **8**      | \[5\] + \[3\]              | 2                   |
| **9**      | \[5\] + \[3\] + \[1\]      | 3                   |

##

## 4. Unidad 2: Suma Somática y la Avalancha por Pasos de Reloj

### Principios Mecánicos: Espacio de Fases y Pasos de Reloj

En la informática somática, la suma se realiza colocando los granos del
nuevo sumando directamente en el tablero junto al valor existente. No es
necesario calcular azares o aterrízajes inmediatamente mientras se
colocan los granos. El operador humano puebla las vasijas (instanciando
el espacio de fases no asentado) y luego "da un paso de reloj" barriendo
sus manos por el tablero para aplicar las reglas locales:

1.  **Fusión en la Fila (Atracción Gravitacional):**

    - **Dos granos \[1\] en la vasija \[1\]:** En el paso de reloj, se
      fusionan en un grano en la vasija \[2\].

    - **Un grano \[1\] y un grano \[2\]:** En el paso de reloj, se
      fusionan en un grano en la vasija \[3\].

    - **Un grano \[2\] y un grano \[3\]:** En el paso de reloj, caen por
      el camino de menor resistencia $\rightarrow$ se fusionan en un
      grano en la vasija \[5\].

2.  **La Gran Avalancha de Granos (Regla de Acarreo):**

    - Cuando la vasija \[5\] acumula **dos granos** ($5 + 5 = 10$),
      ambos granos se fusionan y **saltan al nivel superior como un solo
      grano en \[1\]** ($+ 10$). La vasija \[5\] de la fila actual queda
      en $0$.

| **NIVEL**                  | **\[5\]**     | **\[3\]** | **\[2\]** | **\[1\]**                                     |
|----------------------------|---------------|-----------|-----------|-----------------------------------------------|
| **Nivel Superior (10s)**   | ( )           | ( )       | ( )       | **(●)** *(Gran llevado +1 a la vasija \[1\])* |
| **Activador de Avalancha** | \\            | \\        | \\        | **▲ (5 + 5 = 10 Avalancha)**                  |
| **Nivel de Unidades (1s)** | **(●) + (●)** | ( )       | ( )       | **La vasija \[5\] se vacía a 0**              |

### Procedimiento Directo de Suma en Tablero (A + B)

1.  Configure el número inicial A en la Yupana según la Regla de Oro.

2.  Tome los granos correspondientes al número B en su mano.

3.  Deposite los granos de B directamente en las vasijas
    correspondientes donde se encuentra A (por ejemplo, si B tiene un 5
    en las unidades, coloque un grano en la vasija \[5\] de la fila de
    unidades).

4.  **Paso de Reloj:** Barra con sus manos desde la fila de unidades
    ($10^{0}$) hacia arriba, resolviendo fusiones y avalanchas hasta que
    cada fila cumpla con la Regla de Oro.

##

## 5. Unidad 3: Resta Somática y Destejido (Préstamo)

### Principio Mecánico

La resta es la eliminación física de granos directamente del tablero. Si
una vasija no contiene suficientes granos para retirar el valor del
sustraendo, el operador **desteje** un grano de un nivel superior para
proporcionar la energía necesaria.

**Regla del Destejido (Préstamo):** Retire 1 grano de la vasija \[1\]
del nivel superior ($10^{n + 1}$) y reemplácelo por DOS granos en la
vasija \[5\] del nivel actual ($10^{n}$). ($10 = 5 + 5$).

| **NIVEL**                  | **ACCIÓN / ESTADO DEL GRANO**                                      |
|----------------------------|--------------------------------------------------------------------|
| **Nivel Superior (10s)**   | **(●)** $\rightarrow$ *Retirar 1 grano (-10)*                      |
| **Flujo de Destejido**     | **│** $\rightarrow$ **▼ (Se desteje en 5 + 5)**                    |
| **Nivel de Unidades (1s)** | **(●) (●) en la vasija \[5\]** $\rightarrow$ *¡Restar libremente!* |

### Procedimiento Directo de Resta en Tablero (A - B)

1.  Configure el minuendo A en la Yupana.

2.  Identifique el valor del sustraendo B dígito por dígito.

3.  Retire los granos correspondientes a B comenzando desde el nivel más
    alto hacia abajo. Si a una vasija le falta el grano necesario,
    desteja un grano del nivel superior convirtiéndolo en dos granos
    \[5\] en el nivel actual, y luego retire la cantidad requerida.

##

## 6. Unidad 4: Multiplicación Táctil (El Telar Multiplicador)

### Principio Mecánico

La multiplicación en la Yupana utiliza la traducción espacial entre
filas, tratando los niveles verticales del tablero como "rieles del
telar". No es necesario memorizar las tablas de multiplicar.

### Reglas de Desplazamiento Espacial

Descomponga el multiplicador en sus vasijas componentes individuales
($\lbrack 5\rbrack,\lbrack 3\rbrack,\lbrack 2\rbrack,\lbrack 1\rbrack$ a
través de sus respectivas filas). Para cada componente:

- **Multiplicar por \[1\]:** Replique el patrón del multiplicando en la
  misma fila.

- **Multiplicar por \[2\]:** Duplique el patrón del multiplicando en la
  misma fila.

- **Multiplicar por \[3\]:** Triplique el patrón del multiplicando en la
  misma fila.

- **Multiplicar por \[5\]:** Desplace el patrón del multiplicando UN
  nivel de fila hacia arriba (equivalente a $\times 10$) y tome la
  mitad, O colóquelo en las vasijas \[5\] de la fila desplazada.

- **Multiplicar por Decenas / Centenas (10, 30, etc.):** Desplace todo
  el patrón HACIA ARRIBA 1 o 2 niveles de fila.

Después de colocar todos los granos de los productos parciales
directamente en el tablero, ejecute un solo **Paso de Reloj** para
resolver todas las fusiones y avalanchas hasta que el tablero se
asiente.

##

##

## 7. Unidad 5: División Somática y Reparto Equitativo (***Ayni***)

### Fundamentos Pedagógicos del ***Ayni***

En la cultura andina, el *Ayni* representa el intercambio comunitario
recíproco y la distribución equitativa. La división somática modela esto
directamente: una cosecha comunitaria total (dividendo) se divide
sistemáticamente en asignaciones familiares iguales (divisor).

La división en la Yupana es el **inverso exacto del Telar
Multiplicador**. En lugar de desplazar un multiplicando HACIA ARRIBA
para construir un producto, la división prueba cuántas unidades
completas del divisor se pueden "cosechar" (restar) del dividendo, nivel
por nivel, trabajando de arriba hacia abajo.

### El Protocolo de División Somática de 4 Pasos

| **PASO** | **ACCIÓN**             | **DESCRIPCIÓN**                                                                                                              |
|----------|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| **1**    | **Configuración**      | Coloque el dividendo total en la Yupana. Mantenga el divisor a un lado como plantilla de referencia.                         |
| **2**    | **Probar Capacidad**   | Pruebe si una unidad completa del divisor (escalada al nivel ocupado más alto) cabe en el dividendo.                         |
| **3**    | **Cosechar y Asignar** | Reste el patrón del divisor del tablero y anote 1 conteo en la fila del Cociente para ese nivel.                             |
| **4**    | **Paso Hacia Abajo**   | Desteja los granos restantes hacia abajo ($10^{n} \rightarrow 5 + 5$ en $10^{n - 1}$) y repita hasta completar las Unidades. |

### Ejemplo Detallado de División 1: 4.800 / 32 = 150

- **Estado Inicial:** 4.800 en el tablero (Millares: \[3\]+\[1\],
  Centenas: \[5\]+\[3\]). Divisor de referencia = 32 (3 Decenas, 2
  Unidades).

#### Paso 1: Probar Nivel de Centenas (Escalando Divisor por 100 $\rightarrow$ 3.200)

- ¿Podemos restar 3.200 (3 Millares, 2 Centenas) de 4.800? **¡SÍ!**

- **Acción:** Retire 3 granos de la fila de Millares, 2 granos de la
  fila de Centenas.

- **Restante en Tablero:** 1.600 (Millares: \[1\], Centenas:
  \[5\]+\[1\]).

- **Cociente Registrado:** 1 Centena (100).

#### Paso 2: Probar Nivel de Centenas Nuevamente

- ¿Podemos restar otros 3.200 de 1.600? **NO.**

- **Destejer Millares:** Tome 1 grano de Millares \[1\] y destéjalo en
  DOS granos \[5\] en la fila de Centenas.

- **La fila de Centenas ahora tiene:** \[5\], \[5\], \[5\], \[1\] (=
  1.600).

#### Paso 3: Probar Nivel de Decenas (Escalando Divisor por 10 $\rightarrow$ 320)

- ¿Cuántos 320 (3 Centenas, 2 Decenas) caben en 1.600?

  - 1.ª asignación (-320): Quedan = 1.280. Cociente += 10.

  - 2.ª asignación (-320): Quedan = 960. Cociente += 10.

  - 3.ª asignación (-320): Quedan = 640. Cociente += 10.

  - 4.ª asignación (-320): Quedan = 320. Cociente += 10.

  - 5.ª asignación (-320): Quedan = 0. Cociente += 10.

- **Asignación Total de Decenas:** 50.

**RESULTADO FINAL:** $100 + 50 = 150$ *(Distribución exacta, resto 0)*

### Ejemplo Detallado de División 2: 1.472 / 23 = 64

- **Estado Inicial:** 1.472 en el tablero (Millares: \[1\], Centenas:
  \[3\]+\[1\], Decenas: \[5\]+\[2\], Unidades: \[2\]). Divisor de
  referencia = 23 (2 Decenas, 3 Unidades).

#### Paso 1: Probar Nivel de Centenas (Escalando Divisor por 100 $\rightarrow$ 2.300)

- ¿Podemos restar 2.300 de 1.472? **NO.**

- **Destejer Millares:** Tome 1 grano de Millares \[1\] y destéjalo en
  DOS granos \[5\] en la fila de Centenas.

- **La fila de Centenas ahora tiene:** 1.400 (dos \[5\], un \[3\], un
  \[1\]).

#### Paso 2: Probar Nivel de Decenas (Escalando Divisor por 10 $\rightarrow$ 230)

- ¿Cuántos 230 (2 Centenas, 3 Decenas) caben en 1.472?

  - Probar 60 asignaciones ($6 \times 230 = 1.380$):

  - Restar 1.380 (13 Centenas, 8 Decenas) del tablero.

  - **Restante en Tablero:** 92 (Decenas: \[5\]+\[3\]+\[1\], Unidades:
    \[2\]).

  - **Cociente Registrado:** 60.

#### Paso 3: Probar Nivel de Unidades (Divisor $\rightarrow$ 23)

- ¿Cuántos 23 (2 Decenas, 3 Unidades) caben en 92?

  - Destejer Decenas si es necesario para exponer granos de unidades.

  - 4 asignaciones ($4 \times 23 = 92$).

  - Restar 92 del tablero. **Restante en Tablero:** 0.

  - **Cociente Registrado:** 4.

**RESULTADO FINAL:** $60 + 4 = 64$ *(Distribución exacta)*

## 8. Unidad 6: El Archivo Khipu (Persistencia de Datos)

Una vez que un cálculo se asienta en la Yupana, el estado se registra
permanentemente en una **cuerda colgante de Khipu**:

| **CUERDA PRINCIPAL**        | **Pendiente 1** | **Pendiente 2** | **Pendiente 3** |
|-----------------------------|-----------------|-----------------|-----------------|
| **Millares (**$10^{3}$**)** | ( S )           | ( )             | ( L3 ) 3.000    |
| **Centenas (**$10^{2}$**)** | ( L7 )          | ( S ) Decenas   | ( )             |
| **Unidades (**$10^{0}$**)** | ( E )           | ( L4 )          | ( E )           |
| **VALOR REGISTRADO**        | **1.701**       | **14**          | **3.001**       |

### Codificación de Nudos

1.  **Nudos Simples (S):** Utilizados en el nivel de Millares ($10^{3}$)
    o superior.

2.  **Nudos Largos (L):** Utilizados en Decenas ($10^{1}$) y Centenas
    ($10^{2}$). El número de vueltas en el nudo equivale al dígito (ej.
    $L7 = 7$).

3.  **Nudos en Forma de Ocho (E):** Reservados exclusivamente para el
    nivel de Unidades ($10^{0}$) para representar el valor $1$.

4.  **Espacio Vacío:** Representa un $0$ en la posición posicional
    correspondiente.

## 9. Rúbrica de Evaluación y Verificación para Educadores

| **Habilidad / Objetivo**    | **Principiante (1-2 pts)**                                                               | **Competente (3-4 pts)**                                                           | **Maestro (5 pts)**                                                   |
|-----------------------------|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| **Codificación de Dígitos** | Usa $> 3$ granos por fila o incumple la Regla de Oro.                                    | Codifica dígitos \$0\dots9\$ correctamente con la Regla de Oro.                    | Representa cualquier número de 4 dígitos con el mínimo de granos.     |
| **Suma y Paso de Reloj**    | Olvida fusionar granos o no realiza las avalanchas entre filas durante el paso de reloj. | Ejecuta fusiones y avalanchas con precisión en el tablero.                         | Realiza avalanchas múltiples de forma fluida y autónoma.              |
| **Resta y Destejido**       | Intenta restar en vasijas vacías sin destejer niveles superiores.                        | Desteje correctamente granos de niveles superiores ($10 \rightarrow 5 + 5$).       | Realiza destejidos de varios niveles sin vacilación.                  |
| **División Ayni**           | Le cuesta escalar niveles de divisores o seguir las asignaciones de resta.               | Ejecuta cosechas de arriba hacia abajo y destejidos para hallar cocientes exactos. | Demuestra división fluida y explica la asignación de recursos *Ayni*. |
| **Registro en Khipu**       | Confunde tipos de nudos o niveles posicionales en la cuerda.                             | Traduce valores de la Yupana a nudos de Khipu ($s,L,E$) con precisión.             | Explica cómo la información pasa de la Yupana al Khipu sin pérdidas.  |

## 10. Hojas de Trabajo de Ejemplo Actualizadas

### Hoja de Trabajo 1: Práctica de Codificación

*Marque o coloque los granos en las vasijas para cada número según la
Regla de Oro:*

1.  **Número: 382**

    - Centenas ($10^{2}$): \[5\] ( ) \[3\] (●) \[2\] ( ) \[1\] ( )

    - Decenas ($10^{1}$): \[5\] (●) \[3\] (●) \[2\] ( ) \[1\] ( )

    - Unidades ($10^{0}$): \[5\] ( ) \[3\] ( ) \[2\] (●) \[1\] ( )

2.  **Número: 1.509**

    - Millares ($10^{3}$): \[5\] ( ) \[3\] ( ) \[2\] ( ) \[1\] (●)

    - Centenas ($10^{2}$): \[5\] (●) \[3\] ( ) \[2\] ( ) \[1\] ( )

    - Decenas ($10^{1}$): \[5\] ( ) \[3\] ( ) \[2\] ( ) \[1\] ( )
      *(Vacío)*

    - Unidades ($10^{0}$): \[5\] (●) \[3\] (●) \[2\] ( ) \[1\] (●)

### Hoja de Trabajo 2: Problemas Somáticos (Operaciones en Tablero)

*Resuelva utilizando su tablero Yupana físico (¡sin pilas externas!).
Registre sus pasos intermedios y el estado final del tablero:*

#### Problema 1: Suma

$247 + 385 =$ **\_\_\_\_\_**

- *Paso A:* Coloque 247 en el tablero.

- *Paso B:* Agregue 385 directamente en las vasijas correspondientes.

- *Paso C (Paso de Reloj):* Resuelva fusiones y avalanchas.

- **Respuesta Esperada: 632** *(Centenas: \[5\]+\[1\], Decenas: \[3\],
  Unidades: \[2\])*

#### Problema 2: Resta

$1.204 - 531 =$ **\_\_\_\_\_**

- *Paso A:* Coloque 1.204 en el tablero.

- *Paso B:* Desteja el nivel de Millares ($1.000 \rightarrow 500 + 500$
  en Centenas).

- *Paso C:* Retire 531 directamente.

- **Respuesta Esperada: 673** *(Centenas: \[5\]+\[1\], Decenas:
  \[5\]+\[2\], Unidades: \[3\])*

#### Problema 3: Multiplicación (Telar Multiplicador)

$64 \times 23 =$ **\_\_\_\_\_**

- *Paso A:* Descomponga el multiplicador $23 = 20 + 3$.

- *Paso B:* Coloque $64 \times 2$ desplazado 1 fila hacia arriba
  ($1.280$).

- *Paso C:* Coloque $64 \times 3$ en la misma fila ($192$).

- *Paso D (Paso de Reloj):* Resuelva todas las fusiones/avalanchas.

- **Respuesta Esperada: 1.472** *(Millares: \[1\], Centenas:
  \[3\]+\[1\], Decenas: \[5\]+\[2\], Unidades: \[2\])*

#### Problema 4: División Ayni (Reparto Equitativo)

$3.600/24 =$ **\_\_\_\_\_**

- *Paso A:* Coloque 3.600 en el tablero. Divisor = 24.

- *Paso B (Nivel de Centenas):* Pruebe con 240 ($24 \times 10$). Reste
  $2.400$ ($1 \times 2.400$). Restante = $1.200$. Cociente en Centenas =
  100.

- *Paso C (Nivel de Decenas):* Desteja $1.200$ en Decenas/Centenas.
  Pruebe con 24 ($24 \times 10$). Reste $1.200$ ($5 \times 240$).
  Restante = 0. Cociente en Decenas = 50.

- **Respuesta Esperada: 150** *(Cociente: Centenas \[1\], Decenas
  \[5\])*
