
# FORM-FB-01 — Fichas Bibliográficas

## Información general

**Universidad:** Universidad Técnica Estatal de Quevedo (UTEQ)  
**Asignatura:** Aplicaciones Distribuidas  
**Actividad:** FORM-FB-01  
**Estudiante:** Zambrano Parraga Luis Mario  
**Fecha:** Noviembre de 2026  

## Descripción

Este repositorio contiene las cinco fichas bibliográficas
desarrolladas para la actividad formativa FORM-FB-01,
enfocada en fundamentos de sistemas distribuidos y
arquitecturas de microservicios.

Las fichas incluyen referencias académicas en formato
IEEE, identificadores DOI, resúmenes, datos verificables
y notas de aprendizaje relacionadas con el informe
académico individual TA-IND-01.

## Estructura del repositorio

- `Documento PDF Compilado/`: documento PDF de las fichas.
- `latext (archivo .text y .bib)/`: archivos fuente LaTeX.
- `Referencias (.bib)/`: registros bibliográficos.
- `Referencias (PDF)/`: publicaciones originales consultadas.

## Requisitos de compilación

Para compilar el documento se necesita:

- Una distribución LaTeX, como MiKTeX o TeX Live.
- Compilador pdfLaTeX.
- Procesador bibliográfico Biber.
- Paquetes LaTeX: babel, newtx, microtype, csquotes,
  geometry, array, longtable, fancyhdr, biblatex
  e hyperref.

Se utilizó Visual Studio Code con la extensión
LaTeX Workshop para la edición del documento.

## Instrucciones de compilación

**Archivo principal:** `main.tex`  
**Archivo bibliográfico:** `referencias.bib`  
**Compilador:** pdfLaTeX  
**Procesador de bibliografía:** Biber  

### Paso 1. Obtener el proyecto

Descargar el repositorio desde GitHub mediante
la opción Code > Download ZIP o clonarlo con Git.

### Paso 2. Ubicar los archivos

Abrir una terminal dentro de la carpeta que
contiene `main.tex` y `referencias.bib`.

Ambos archivos deben encontrarse en la misma
carpeta para utilizar la configuración actual.

### Paso 3. Ejecutar los comandos

Ejecutar los siguientes comandos en este orden:

```powershell
pdflatex main.tex
biber main
pdflatex main.tex
pdflatex main.tex
```

La primera ejecución procesa el documento.
Biber genera las referencias bibliográficas IEEE.
Las dos ejecuciones finales actualizan las
referencias, citas y elementos del documento.

### Paso 4. Consultar el resultado

Al finalizar correctamente la compilación se
genera el archivo `main.pdf`.

También se incluye una versión compilada en
la carpeta `Documento PDF Compilado`.

## Gestión bibliográfica

Las referencias se administran mediante un
archivo `.bib` utilizando `biblatex` con
el estilo `ieee` y el procesador `biber`.

Las cinco publicaciones cuentan con DOI y
corresponden al período 2021–2026.

## Finalidad académica

Este trabajo constituye una actividad formativa
preparatoria para el informe individual TA-IND-01.

La información bibliográfica recopilada servirá
como base para el análisis crítico de un sistema
distribuido real.
