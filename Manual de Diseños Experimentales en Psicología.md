

# 📘 **Manual de Diseños Experimentales en Psicología**  
**Arnau Gras, J. — Catedrático Emérito, Universidad de Barcelona**

---

## Introducción

El objetivo de esta página es facilitar el análisis de datos para los diseños experimentales más comunes en las ciencias sociales y de la salud, especialmente en psicología y educación. Se pretende resolver de manera rápida y sin dificultades el problema de obtener resultados científicos sin recurrir a programas estadísticos complejos como SPSS, SAS, Minitab o R.

Para ello se ofrecen varias aplicaciones web que permiten realizar análisis experimentales sin necesidad de conocimientos avanzados de programación.

---

## Acceso a las aplicaciones

### 1. Diseños Experimentales Clásicos  
**URL:** https://jarnau.shinyapps.io/disexpsy/  
Contiene los diseños experimentales clásicos utilizados en psicología.

### 2. Diseños de Medidas Repetidas  
**URL:** https://jarnau.shinyapps.io/disexpsy-mr/  
Centrada en los diseños de medidas repetidas.

### 3. Diseños de Caso Único  
**URL:** https://jarnau.shinyapps.io/discupsy/  
Permite analizar diseños de caso único propios del ámbito clínico y educativo.

### 4. Generador de Datos  
**URL:** https://jarnau.shinyapps.io/creardisexpsy/  
Genera datos simulados para los diseños anteriores.

---

# Consideraciones Generales sobre los Diseños Experimentales

Los diseños experimentales se estructuran en torno a las siguientes variables:

- **Variable dependiente**: valores de respuesta.  
- **Variable independiente**: manipulada por el investigador.  
- **Variable de sujeto (ID)**: identifica a cada participante.  
- **Covariables**: edad, nivel socioeconómico, etc.

La variable independiente puede ser:

- **Entre sujetos**: valores distintos para grupos distintos.  
- **Intra sujetos**: los mismos valores para todos los sujetos (medidas repetidas).

### Diseño de Caso Único

- Las sesiones de observación forman las fases.  
- Las fases representan niveles de la variable independiente.  
- La unidad de observación puede ser un individuo o un grupo.  
- Se pueden analizar varios tratamientos y sus interacciones.

---

# Creación de Archivos de Datos (CSV)

Para crear un archivo CSV en Excel:

1. Crear columnas y etiquetarlas.  
2. Ir a **Datos → Texto en columnas**.  
3. Seleccionar **delimitado por comas**.  
4. Guardar como **CSV (delimitado por comas)**.  
5. Verificar abriendo el archivo en un editor de texto.

El formato CSV es estándar y compatible con Excel, R, Python, SPSS, MATLAB y las aplicaciones Shiny.

---

# Modelos de Análisis de Diseños Experimentales

---

## 1. Diseño de Grupos (One-Way ANOVA)

Modelo:

\[
Y = \mu + A_i + \varepsilon
\]

- \(Y\): variable dependiente  
- \(A_i\): efecto del grupo  
- \(\varepsilon\): error aleatorio  

### Análisis  
Se aplica un **ANOVA unifactorial** para comparar medias entre grupos.

### Supuestos

1. **Independencia** de las observaciones.  
2. **Normalidad** de la variable dependiente.  
3. **Homoscedasticidad** (varianzas iguales).  
4. **Escala adecuada**: VD continua, VI categórica.

---

## 2. Diseño Factorial (Two-Way ANOVA)

Modelo:

\[
Y = \mu + A_i + B_j + (A \times B)_{ij} + \varepsilon
\]

Permite estudiar efectos principales e interacción entre dos factores.

### Supuestos

- Independencia  
- Normalidad  
- Homogeneidad de varianzas  
- Factores categóricos  
- Interacción interpretable

---

## 3. Diseño de Medidas Repetidas

Modelo:

\[
Y = \mu + A_i + S_k + (A \times S)_{ik} + \varepsilon
\]

- \(A_i\): factor intra-sujetos  
- \(S_k\): variabilidad entre sujetos  

### Análisis  
ANOVA de medidas repetidas con prueba de esfericidad de Mauchly.

### Supuestos

- Independencia entre sujetos  
- Normalidad  
- Esfericidad  
- Escala adecuada

---

## 4. Diseño Factorial de Medidas Repetidas

Modelo:

\[
Y = \mu + A_i + B_j + (A \times B)_{ij} + S_k + (A \times S)_{ik} + (B \times S)_{jk} + (A \times B \times S)_{ijk} + \varepsilon
\]

Permite analizar dos factores intra-sujetos y su interacción.

---

## 5. Diseño Factorial Mixto (Mixed ANOVA)

Modelo:

\[
Y = \mu + A_i + B_j + (A \times B)_{ij} + S_k + (B \times S)_{jk} + \varepsilon
\]

- \(A\): factor entre sujetos  
- \(B\): factor intra sujetos  

### Análisis  
Modelo lineal mixto (LMM).

---

## 6. Diseño Split-Plot

Modelo:

\[
Y = \mu + A_i + B_j + (A \times B)_{ij} + S_k + (A \times S)_{ik} + \varepsilon
\]

- \(A\): factor entre sujetos  
- \(B\): factor intra sujetos  

---

# Cómo Introducir las Variables en la App

## Diseño de Grupos
- **Y**: variable dependiente  
- **X**: factor  
- **Random**: —  
- **Entre / Intra**: —  

## Diseño Factorial
- **Y**  
- **X**: factor1, factor2  
- **Random**: —  

## Medidas Repetidas
- **Y**  
- **X**: factor repetido  
- **Random**: sujeto  

## Factorial de Medidas Repetidas
- **Y**  
- **X**: factor1, factor2  
- **Random**: sujeto  

## Diseño Mixto
- **Y**  
- **X**: factor1, factor2  
- **Random**: sujeto  
- **Entre**: factor entre sujetos  
- **Intra**: factor intra sujetos  

## Split-Plot
- **Y**  
- **X**: factor1 (entre), factor2 (intra)  
- **Random**: sujeto  

---

