# FORM-FB-01 — Fichas bibliográficas

**Autor:** Byron Daniel Loor Mendoza  
**Actividad:** Fundamentos de sistemas distribuidos y arquitecturas distribuidas  
**Modalidad:** Individual  
**Periodo:** Noviembre de 2026

## Descripción

Documento con cinco fichas bibliográficas sobre tolerancia a fallos, recuperación del estado, disponibilidad, diagnóstico de anomalías y consistencia en sistemas distribuidos. Las fuentes constituyen una base para el análisis de Fission en TA-IND-01.

Cada ficha incluye el DOI, una síntesis de 100 palabras, un hallazgo con su localización y una valoración crítica de la fuente. Las referencias se generan con `biblatex`, estilo IEEE y backend Biber. La declaración de uso de inteligencia artificial se encuentra al final del documento, antes de las referencias.

## Organización de archivos

| Ruta | Contenido |
| --- | --- |
| `Documento/FORM_FB_01_Byron_Loor.pdf` | PDF de las cinco fichas. |
| `LaTeX/main.tex` | Documento principal en LaTeX. |
| `LaTeX/referencias.bib` | Las cinco entradas utilizadas para generar la bibliografía. |
| `README.md` | Descripción e instrucciones de compilación. |
| `Fuentes/` | Los artículos consultados en PDF y sus exportaciones bibliográficas individuales en `.bib`. |

`main.tex` y `referencias.bib` deben permanecer juntos en `LaTeX/`. El material de `Fuentes/` es complementario; el archivo bibliográfico que utiliza el documento es `LaTeX/referencias.bib`.

## Compilación

### Requisitos

| Elemento | Configuración |
| --- | --- |
| Archivo principal | `LaTeX/main.tex` |
| Compilador | pdfLaTeX |
| Bibliografía | Biber, con `biblatex` y estilo IEEE |

Para compilar en el equipo se necesita TeX Live o MiKTeX con soporte para español. Los archivos deben guardarse en UTF-8.

**Paquetes utilizados:** `inputenc`, `fontenc`, `babel` (español), `geometry`, `csquotes`, `microtype`, `titlesec`, `needspace`, `biblatex`, `biblatex-ieee` y `hyperref`.

### Compilación local

Desde la carpeta de esta actividad, ejecutar en este orden:

```bash
cd LaTeX
pdflatex main.tex
biber main
pdflatex main.tex
pdflatex main.tex
```

El resultado es `LaTeX/main.pdf`. Para la entrega, guardar una copia en `Documento/` con el nombre `FORM_FB_01_Byron_Loor.pdf`.

### En Overleaf

1. Subir al mismo proyecto los archivos `main.tex` y `referencias.bib` que se encuentran en `LaTeX/`.
2. Seleccionar `main.tex` como archivo principal y pdfLaTeX como compilador.
3. Pulsar **Recompile** y comprobar que aparecen las cinco referencias.
4. Descargar el PDF como `FORM_FB_01_Byron_Loor.pdf` y guardarlo en `Documento/`.

## Fuentes y acceso al texto completo

| Ficha | Fuente | DOI | PDF gratuito |
| --- | --- | --- | --- |
| 1 | Bouizem y colaboradores, 2023. *Integrating request replication into FaaS platforms: an experimental evaluation*. | [10.1186/s13677-023-00457-z](https://doi.org/10.1186/s13677-023-00457-z) | [Texto completo](https://link.springer.com/content/pdf/10.1186/s13677-023-00457-z.pdf) |
| 2 | Fragkoulis y colaboradores, 2024. *A survey on the evolution of stream processing systems*. | [10.1007/s00778-023-00819-8](https://doi.org/10.1007/s00778-023-00819-8) | [Texto completo](https://link.springer.com/content/pdf/10.1007/s00778-023-00819-8.pdf) |
| 3 | Kokociński, Kobus y Wojciechowski, 2023. *On the correctness of highly available systems in the presence of failures*. | [10.1016/j.jpdc.2023.04.008](https://doi.org/10.1016/j.jpdc.2023.04.008) | [Texto completo](https://www.cs.put.poznan.pl/pawelw/pdf/jpdc23-journal-full.pdf) |
| 4 | Barata y colaboradores, 2026. *Anomaly detection and root-cause identification in microservices: a survey*. | [10.1007/s10586-026-06095-9](https://doi.org/10.1007/s10586-026-06095-9) | [Texto completo](https://link.springer.com/content/pdf/10.1007/s10586-026-06095-9.pdf) |
| 5 | Bação y Guerreiro, 2026. *Consistency challenges in event-driven microservices: a literature review on data, process, and system evolution*. | [10.1007/s00607-026-01701-5](https://doi.org/10.1007/s00607-026-01701-5) | [Texto completo](https://link.springer.com/content/pdf/10.1007/s00607-026-01701-5.pdf) |

La primera fuente evalúa Fission directamente. Las otras cuatro aportan fundamentos para el análisis; sus resultados no se atribuyen automáticamente a esa plataforma.
