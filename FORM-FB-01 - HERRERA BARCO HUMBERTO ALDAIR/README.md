# Fichas bibliográficas: fundamentos de sistemas distribuidos y arquitecturas distribuidas

Documento en LaTeX con la portada, las fichas bibliográficas, la declaración de uso de inteligencia artificial y la lista de referencias en formato IEEE.

**Autor:** Herrera Barco Humberto Aldair
**Carrera:** Ingeniería en Software, Facultad de Ciencias de la Computación, Universidad Técnica Estatal de Quevedo (UTEQ)

## Archivos del proyecto

| Archivo | Descripción |
|---|---|
| `fichas.tex` | **Archivo principal.** Contiene la portada, las fichas 01 a 05 y la declaración de uso de IA. |
| `fuentes.bib` | Base de datos de referencias (BibTeX). Se usa con estilo IEEE. |
| `fichas.pdf` | Resultado de la compilación (se genera al compilar). |

Ambos archivos deben estar en la **misma carpeta**. El documento no usa imágenes.

## Compilador

**pdfLaTeX** (TeX Live 2020 o más reciente). Para la bibliografía se usa **BibTeX**, no Biber.

## Orden de compilación

Ejecuta estos comandos en la carpeta del proyecto, en este orden:

```bash
pdflatex fichas.tex
bibtex fichas
pdflatex fichas.tex
pdflatex fichas.tex
```

Cada paso hace algo distinto:

1. `pdflatex` (primera vez): lee el documento y anota las citas que usa.
2. `bibtex`: busca esas citas en `fuentes.bib` y arma la lista de referencias. Se escribe **sin extensión** (`fichas`, no `fichas.tex`).
3. `pdflatex` (segunda vez): inserta la lista de referencias en el documento.
4. `pdflatex` (tercera vez): corrige los números de las citas.

Si te saltas pasos, las citas salen como `[?]`.

### Alternativa con un solo comando

Con `latexmk` (viene con TeX Live) se hacen todos los pasos solos:

```bash
latexmk -pdf fichas.tex
```

Para borrar los archivos temporales: `latexmk -c`.

### En Overleaf

1. Sube `fichas.tex` y `fuentes.bib` a un proyecto nuevo.
2. En **Menú → Compiler**, elige **pdfLaTeX**.
3. En **Menú → Main document**, elige `fichas.tex`.
4. Presiona **Recompile**. Overleaf ejecuta BibTeX automáticamente.

## Dependencias

Paquetes de LaTeX que usa `fichas.tex`:

| Paquete | Para qué |
|---|---|
| `inputenc`, `fontenc` | Tildes y caracteres en español |
| `babel` (opción `spanish`) | Idioma del documento |
| `mathptmx` | Fuente tipo Times New Roman |
| `geometry` | Márgenes |
| `hyperref`, `url` | Enlaces de los DOI |
| `xcolor` | Color de los textos pendientes |
| `IEEEtran` (estilo `.bst`) | Formato IEEE de las referencias |

Overleaf ya los trae todos. Si compilas en tu computador y falta alguno:

**Linux (Debian/Ubuntu):**

```bash
sudo apt install texlive-latex-base texlive-latex-recommended texlive-latex-extra \
                 texlive-fonts-recommended texlive-lang-spanish texlive-publishers
```

`texlive-lang-spanish` aporta el idioma español y `texlive-publishers` aporta `IEEEtran`.

**Windows / macOS:** instala [MiKTeX](https://miktex.org/) o [MacTeX](https://tug.org/mactex/). Instalan los paquetes que faltan al compilar, o ya vienen incluidos.
