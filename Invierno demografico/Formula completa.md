A continuación se presenta la formulación formal del modelo $\Psi_3$, con notación clara en español y definición estadística de cada parámetro.

---

# 📘 Modelo $\Psi_3$: Índice Estructural de Potencial Reproductivo

## 1. Definición Formal

Sea el índice estructural de potencial reproductivo definido como:

$
\Psi_3 =
\frac{
(DES \cdot SAL_f \cdot SAL_m)\cdot(1 + REL)\cdot(1 - INC)\cdot CAP \cdot EST
}{
(VIV \cdot OPP_f \cdot OPP_m) + (DIG \cdot IND)^2 + ESTS
}
$

donde:

* $\Psi_3 \in \mathbb{R}^+$
* $\Psi_3 > 1$ → condiciones estructurales compatibles con reemplazo generacional
* $\Psi_3 < 1$ → presión estructural hacia descenso de fecundidad

---

# 2. Estructura del Modelo

El modelo se divide en dos bloques:

Numerador → Factores habilitantes
Denominador → Factores restrictivos

---

# 3. Definición y Anclaje Estadístico de Variables

## 3.1 Numerador

### (1) $DES$ — Deseo reproductivo normalizado

$
DES = \frac{h_d}{2.1}
$

donde:

$h_d$ = número promedio de hijos deseados según encuestas nacionales de fecundidad.

Fuentes:

* DHS (Demographic and Health Surveys)
* ENADID (México)
* OECD Family Database
* World Bank Fertility Preferences

Interpretación:

* $DES > 1$ → deseo superior al nivel de reemplazo.
* $DES < 1$ → deseo inferior al reemplazo.

---

### (2) $SAL_f$ — Salud femenina en edad fértil (0–1)

Índice compuesto normalizado:

$
SAL_f = 1 - \frac{1}{4}(O_f + INF_f + M_f + RET_f)
$

donde:

$O_f$ = prevalencia de obesidad femenina (OMS)
$INF_f$ = prevalencia de infertilidad femenina (OMS, ~17% global promedio)
$M_f$ = mortalidad materna relativa (WHO)
$RET_f$ = retraso promedio del primer parto respecto a edad óptima biológica (~25 años)

Fuentes:

* WHO Global Health Observatory
* World Bank Health Data

---

### (3) $SAL_m$ — Salud masculina fértil (0–1)

$
SAL_m = 1 - \frac{1}{3}(O_m + TAB_m + INF_m)
$

donde:

$O_m$ = obesidad masculina
$TAB_m$ = tasa de tabaquismo masculino
$INF_m$ = proxy de deterioro espermático (meta-análisis globales reportan caída $>50\%$ desde 1973 en Occidente)

Fuentes:

* WHO
* The Lancet
* Human Reproduction Update

---

### (4) $REL$ — Religiosidad estructural (0–1)

$
REL = \frac{p_{rel}}{p_{rel}^{max}}
$

donde:

$p_{rel}$ = porcentaje que declara que la religión es “muy importante” (Pew Research, World Values Survey)

---

### (5) $INC$ — Índice de incertidumbre percibida (0–1)

Índice compuesto:

* Desempleo juvenil
* Índice de confianza del consumidor
* Riesgo percibido de inseguridad
* Vulnerabilidad climática

Fuentes:

* OECD
* World Bank
* Gallup World Poll

---

### (6) $CAP$ — Capital social familiar (0–1)

Proxies:

* % hogares multigeneracionales
* Disponibilidad de apoyo informal para cuidado infantil
* Índice de confianza interpersonal

Fuentes:

* World Values Survey
* OECD Social Indicators

---

### (7) $EST$ — Estabilidad de pareja (0–1)

$
EST = 1 - (DIV + SINP)
$

donde:

$DIV$ = tasa de divorcio normalizada
$SINP$ = proporción de adultos que nunca forman pareja estable

Fuentes:

* OECD Family Database
* Registros civiles nacionales

---

# 3.2 Denominador

### (8) $VIV$ — Costo relativo de vivienda

$
VIV = \frac{Precio\ vivienda / Ingreso\ anual}{5}
$

5 se toma como umbral estructural de accesibilidad.

Fuentes:

* Numbeo
* World Bank Housing Affordability Indicators
* OECD Housing Data

---

### (9) $OPP_f$ — Costo oportunidad femenino (0–1)

Índice compuesto:

* % mujeres con educación terciaria
* Tasa participación laboral femenina
* Brecha salarial
* Edad media al primer hijo

Fuentes:

* World Bank Gender Data
* OECD Gender Statistics

---

### (10) $OPP_m$ — Costo oportunidad masculino (0–1)

Proxies:

* Desempleo masculino joven
* Ingreso real mediano estancado
* Precarización laboral

Fuentes:

* ILOSTAT
* OECD Employment Data

---

### (11) $DIG$ — Intensidad digital (0–1)

* % penetración internet
* Horas promedio diarias en redes sociales

Fuentes:

* ITU
* DataReportal
* World Bank ICT Indicators

---

### (12) $IND$ — Individualismo cultural (0–1)

Basado en índice Hofstede:

$
IND = \frac{IDV}{100}
$

---

### (13) $ESTS$ — Estrés estructural crónico (0–1)

Índice compuesto:

* Horas promedio trabajadas (OECD)
* Tiempo promedio de traslado urbano
* Tasa de criminalidad
* Carga laboral parental

---

# 4. Propiedades Matemáticas del Modelo

1. $\Psi_3$ es estrictamente positivo.
2. Sensible no linealmente al bloque digital debido al término cuadrático:
   $
   (DIG \cdot IND)^2
   $
3. Multiplicatividad en el numerador implica que deterioro severo en $SAL_f$ o $SAL_m$ reduce estructuralmente el potencial.
4. Interacción triple en costos económicos:
   $
   VIV \cdot OPP_f \cdot OPP_m
   $
   captura efecto sinérgico de presión dual.

---

# 5. Interpretación Sistémica

El modelo integra tres dimensiones:

* Biológica ($SAL_f$, $SAL_m$)
* Cultural ($REL$, $IND$, $CAP$, $EST$)
* Económica-estructural ($VIV$, $OPP_f$, $OPP_m$, $ESTS$)

No pretende sustituir modelos demográficos clásicos (como cohort-component), sino ofrecer un índice estructural comparativo que explica por qué sociedades con igual PIB per cápita pueden tener fecundidades radicalmente distintas.

---

# 6. Limitaciones Técnicas

* Normalización depende de escalas comparativas.
* Algunas variables son proxies indirectos (ej. deterioro espermático).
* No modela migración neta.
* No incorpora políticas públicas específicas (licencias parentales, subsidios directos).

---

# 7. Posible Extensión

Modelo dinámico:

$
\Psi_3(t+1) = \Psi_3(t) + \alpha \Delta SAL - \beta \Delta OPP + \gamma \Delta CAP
$

Permitirá simulaciones temporales.
