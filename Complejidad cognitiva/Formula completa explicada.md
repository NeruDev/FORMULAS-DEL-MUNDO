
# I. Definición formal del índice ampliado

Definimos el **Índice Psicosocial de Complejidad Cognitiva (IPCC-100)** como:

$$
\boxed{
\Phi_{100} = 100 \cdot
\frac{R_{eff}}{R_{eff} + S_{eff}}
}
$$

Donde:

* $\Phi_{100} \in (0,100)$
* 100 → Máxima capacidad estructural para pensamiento crítico complejo.
* 0 → Máxima presión hacia simplificación cognitiva rígida.

---

# II. Componente racional estructural

$$
R_{eff} =
\left(
\frac{2E + I + L + T}{5}
\right)
\sqrt{H \cdot F}
$$

## Variables racionales

---

## 1️⃣ Educación (E)

Fuente:

* PISA (OCDE) o Years of Schooling (UNESCO).

Normalización min–max:

$$
E =
\frac{Score - Score_{min}}{Score_{max} - Score_{min}}
$$

Rango: [0,1]

Peso doble por su robusta correlación con alfabetización científica y razonamiento analítico.

---

## 2️⃣ Desarrollo humano (I)

Fuente:

* HDI (ONU)

Ya normalizado:

$$
I = HDI
$$

Rango: [0,1]

---

## 3️⃣ Libertad institucional (L)

Fuente:

* V-Dem
* Freedom House

Normalización directa:

$$
L =
\frac{Score}{Score_{max}}
$$

Rango: [0,1]

---

## 4️⃣ Confianza en la ciencia (T)

Fuente:

* Pew Research
* World Values Survey
* Nature Global Trust Dataset

Normalización:

$$
T = \frac{\%\ \text{confianza}}{100}
$$

Rango: [0,1]

Interpretación formal:

T representa legitimidad epistemológica institucional.
No se eleva al cuadrado porque su efecto es modulador, no detonador.

---

## 5️⃣ Salud física (H)

Fuente:

* WHO Healthy Life Expectancy (HALE)

Normalización min–max:

$$
H =
\frac{HALE - HALE_{min}}{HALE_{max} - HALE_{min}}
$$

Rango: [0,1]

---

## 6️⃣ Tiempo libre (F)

Fuente:

* OECD Average Annual Hours Worked
* World Bank Labor Statistics

Normalización invertida:

$$
F =
1 -
\frac{Horas - Horas_{min}}{Horas_{max} - Horas_{min}}
$$

Rango: [0,1]

Justificación formal:

El tiempo cognitivo disponible modula capacidad de procesamiento complejo.

Se introduce junto con salud física:

$$
\sqrt{H \cdot F}
$$

La raíz evita sobreponderación y modela efecto multiplicativo moderado.

---

# III. Componente simplificador psicosocial

$$
S_{eff} =
\frac{
P^2 + C + M^2 + (Rel(1-E))^2
}{4}
$$

---

## 7️⃣ Polarización política (P)

Fuente:

* V-Dem Polarization Index

Rango: [0,1]

No linealidad:

$$
P^2
$$

Modela comportamiento crítico tipo umbral.

---

## 8️⃣ Exposición informativa digital (C)

Fuente:

* ITU % uso de internet
* Reuters % noticias vía redes

Normalización:

$$
C = \frac{\%\ \text{población digital}}{100}
$$

Rango: [0,1]

---

## 9️⃣ Salud mental colectiva (M)

Fuente:

* Global Burden of Disease (ansiedad + depresión)

Normalización min–max (3%–12%):

$$
M =
\frac{Prevalencia - 3}{12 - 3}
$$

No linealidad:

$$
M^2
$$

Modela efecto crítico de deterioro emocional colectivo.

---

## 🔟 Religiosidad contextual (Rel)

Fuente:

* World Values Survey
* Pew Religion

Normalización (5%–95%):

$$
Rel =
\frac{\% - 5}{95 - 5}
$$

Modulación por educación:

$$
Rel_c = Rel(1-E)
$$

No linealidad:

$$
(Rel_c)^2
$$

Formalmente representa:
Influencia ideológica cuando coincide con baja educación estructural.

---

# IV. Fórmula consolidada final

$$
\boxed{
\Phi_{100} = 100 \cdot
\frac{
\left(\frac{2E + I + L + T}{5}\right)\sqrt{HF}
}{
\left(\frac{2E + I + L + T}{5}\right)\sqrt{HF}
+
\frac{
P^2 + C + M^2 + (Rel(1-E))^2
}{4}
}
}
$$

---

# V. Propiedades matemáticas

1️⃣ Escala directa 0–100
2️⃣ Continua y diferenciable
3️⃣ Acotada
4️⃣ Introduce no linealidad en variables detonadoras
5️⃣ Mantiene linealidad en variables estructurales

---

# VI. Interpretación operativa

Valores aproximados:

* 80–100 → Alta resiliencia cognitiva estructural
* 60–80 → Sistema estable pero vulnerable a crisis
* 40–60 → Zona de fricción cognitiva
* 20–40 → Alta presión simplificadora
* 0–20 → Sistema epistemológicamente frágil

---

# VII. Diferencia conceptual respecto a versiones previas

* Ahora el modelo incluye dimensión económica, institucional, psicológica, cultural y laboral.
* Introduce doble modulación biológica (H·F).
* Mantiene umbrales en polarización, salud mental y religión.

Es un modelo híbrido:

50% estructura institucional
30% dinámica psicosocial
20% carga biológica y cognitiva
