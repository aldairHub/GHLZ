# FORM-FB-01 Fichas bibliográficas sobre sistemas distribuidos

**Autor**  
García Bazurto Kevin Leonel

**Asignatura**  
Aplicaciones Distribuidas

## Archivos

- `fichas.tex` — archivo principal en LaTeX con las cinco fichas bibliográficas.
- `referencias.bib` — base bibliográfica utilizada por `biblatex` para generar las referencias en estilo IEEE.
- `FORM_FB_01_Overleaf.pdf` — PDF compilado disponible en esta carpeta.

## Compilación

El documento usa **pdfLaTeX** como compilador y **Biber** para procesar las referencias. Requiere `fontenc` con codificación T1, `babel` con soporte para español, `newtxtext`, `geometry`, `csquotes`, `biblatex`, el estilo `biblatex-ieee` e `hyperref`.

Abre una terminal en esta carpeta, donde están `fichas.tex` y `referencias.bib`, y ejecuta los siguientes comandos en orden.

```sh
pdflatex fichas.tex
biber fichas
pdflatex fichas.tex
pdflatex fichas.tex
```

La compilación genera `fichas.pdf` en la misma carpeta.
