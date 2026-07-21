# Riesgo Ambiental: Fundamentos y Metodología de la Evaluación del Riesgo por Tóxicos Atmosféricos

Presentación académica (LaTeX/Beamer) sobre los fundamentos teóricos y metodológicos de la **Evaluación de Riesgo (ER)** por exposición a tóxicos atmosféricos, desarrollada por el **Dr. José Agustín García Reynoso**, del Instituto de Ciencias de la Atmósfera y Cambio Climático (ICAyCC), UNAM.

El material cubre el proceso completo de análisis de riesgo — desde la identificación del peligro hasta la caracterización del riesgo y su comunicación — con definiciones, formulación matemática y ejemplos numéricos resueltos paso a paso, pensado como apoyo didáctico para cursos universitarios de ciencias atmosféricas, salud ambiental o ingeniería ambiental.

## Contenido de la presentación

La presentación (`Riesgo.tex`) está organizada en las siguientes secciones:

1. **Introducción al Análisis de Riesgo** — origen histórico y aplicación en salud humana y ambiental.
2. **Terminología** — peligro, riesgo, exposición, efectos en salud, percepción del riesgo.
3. **Unidades y Factores** — URF, IPF, ASF, factor de dilución (χ/Q), entre otros.
4. **Metodología de Análisis de Riesgo** (4 etapas):
   - Identificación del peligro (carcinógenos y no carcinógenos, tablas OEHHA/ARB)
   - Evaluación de la exposición (rutas obligatorias y sitio-específicas, modelos matemáticos)
   - Evaluación de dosis-respuesta (CPF vs. REL)
   - Caracterización del riesgo (riesgo de cáncer, Índice de Peligro/HI)
5. **Bioconcentración, bioacumulación y biomagnificación** — rutas de vegetación, pescado y carne.
6. **Riesgo a Ecosistemas** — biodiversidad, AOT40.
7. **Modelos de Evaluación de Riesgos** — HRA 92, ACE2, TOXLT/TOXST, HEM-II, CalTOX, AERAM, TRUE.
8. **Comunicación del Riesgo** — principios y buenas prácticas para comunicar información técnica al público.
9. **Fuente y Dispersión** — fuentes puntuales, factores de emisión, mediciones en chimenea, ecuación de dispersión gaussiana.

A lo largo del material se incluyen ejemplos numéricos resueltos (cálculo de dosis, LCP/PCTV, Índice de Riesgo, exposición multiruta, bioconcentración, dispersión gaussiana, etc.), útiles como ejercicios de clase o autoevaluación.

## Estructura del repositorio

```
riesgoamb/
├── Riesgo.tex        # Código fuente LaTeX (Beamer) de la presentación
├── Riesgo.pdf         # Presentación compilada, lista para usarse
├── contable.pdf        # Material/tabla de apoyo complementario
├── CCA.png            # Logo del ICAyCC (usado en la portada)
├── proceso.png          # Diagrama: etapas del análisis de riesgo
├── rutas.png           # Diagrama: rutas de exposición del contaminante
└── LICENSE            # GPL-3.0
```

## Requisitos

Para compilar `Riesgo.tex` necesitas una distribución de LaTeX (TeX Live, MiKTeX o similar) con los siguientes paquetes:

- `beamer` (tema `Madrid`, color `whale`)
- `babel` (idioma `spanish`)
- `inputenc`
- `amsmath`, `amssymb`, `amsfonts`
- `graphicx`
- `booktabs`
- `multirow`
- `array`
- `colortbl`
- `xcolor`

Todos estos paquetes están incluidos en cualquier instalación estándar de **TeX Live** (`texlive-full`) o **MiKTeX**.

## Compilación

Clona el repositorio y compila con `pdflatex` (se recomienda ejecutarlo dos veces para generar correctamente el índice y las referencias):

```bash
git clone https://github.com/JoseAgustin/riesgoamb.git
cd riesgoamb
pdflatex Riesgo.tex
pdflatex Riesgo.tex
```

Esto generará `Riesgo.pdf` a partir del código fuente. Asegúrate de que `CCA.png`, `proceso.png` y `rutas.png` estén en el mismo directorio que `Riesgo.tex`, ya que se incluyen directamente en las diapositivas.

Alternativamente, puedes usar `latexmk` para automatizar el proceso:

```bash
latexmk -pdf Riesgo.tex
```

## Uso

- **`Riesgo.pdf`** puede utilizarse directamente para impartir la clase o taller sin necesidad de compilar nada.
- **`Riesgo.tex`** puede editarse y adaptarse libremente (agregar ejemplos, actualizar valores de referencia REL/URF, cambiar el idioma, etc.) conforme a los términos de la licencia.
- Las diapositivas incluyen notas (`\note{...}`) pensadas para el instructor, visibles en el modo presentador de Beamer (`\usepackage{pgfpages}` + modo *Notes on second screen*, si se desea habilitar).

## Público objetivo

Este material está dirigido a estudiantes y profesionales de:

- Ciencias atmosféricas y ambientales
- Ingeniería ambiental y salud pública
- Toxicología ambiental
- Cursos de evaluación de impacto ambiental

## Referencia relacionada

Este repositorio es material de apoyo para la siguiente propuesta didáctica publicada por los autores, específicamente sobre la enseñanza de la evaluación de riesgos para la salud por sustancias tóxicas atmosféricas:

> Altúzar Villatoro, F., & García Reynoso, J. A. (2025). Propuesta didáctica sobre evaluación de riesgos para la salud de las sustancias tóxicas atmosféricas. *Educación Química*, 36(1), 41-52. https://doi.org/10.22201/fq.18708404e.2025.1.88739
>
> Disponible en: https://www.revistas.unam.mx/index.php/req/article/view/88739/79357

## Licencia

Este proyecto está distribuido bajo la licencia **GPL-3.0**. Consulta el archivo [`LICENSE`](./LICENSE) para más detalles.

## Autor

**Dr. José Agustín García Reynoso**
Instituto de Ciencias de la Atmósfera y Cambio Climático (ICAyCC), UNAM
📧 agustin@atmosfera.unam.mx

## Cómo citar

Si utilizas este material en un curso o publicación, se agradece la referencia:

> García Reynoso, J. A. *Fundamentos y Metodología de la Evaluación del Riesgo por Tóxicos Atmosféricos: De la Fuente a la Estimación del Impacto en Salud*. Instituto de Ciencias de la Atmósfera y Cambio Climático, UNAM. Disponible en: https://github.com/JoseAgustin/riesgoamb
