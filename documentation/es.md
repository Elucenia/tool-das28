<!-- ELUCENIA technical documentation · das28 · es · no clinical/professional/rights approval -->

# DAS28 (VSG y PCR)

[condiciones, fuentes y permisos](https://elucenia.org/es/herramientas/das28)

## Cómo usar

Utilice la herramienta en el portal o abra index.html mediante un servidor HTTP local. Seleccione el idioma, complete los campos y calcule.

## Entradas y unidades

### Articulaciones dolorosas (de 28)

`tjc`

intervalo: 0–28

### Articulaciones inflamadas (de 28)

`sjc`

intervalo: 0–28

### Evaluación global de salud del paciente (escala visual)

`gh`

mm · intervalo: 0–100

### Velocidad de sedimentación globular (VSG)

`vhs`

mm/h · opcional · intervalo: 1–150

### Proteína C reactiva (PCR)

`pcr`

mg/L · opcional · intervalo: 0–300

## Edición del método

DAS28-VSG/Prevoo 1995 y DAS28-PCR/Wells 2009; 28 articulaciones; intercepto PCR 0,96

## Fórmula documentada

DAS28-VSG = 0,56 × √(dolorosas) + 0,28 × √(tumefactas) + 0,70 × ln(VSG) + 0,014 × valoración global.

DAS28-PCR = 0,56 × √(dolorosas) + 0,28 × √(tumefactas) + 0,36 × ln(PCR + 1) + 0,014 × valoración global + 0,96 (PCR en mg/L).

## Límites y población

El DAS28 de 1995 se desarrolló para la actividad de la artritis reumatoide, utilizando el recuento de 28 articulaciones y comparaciones con la evaluación clínica de reumatólogos. La variante por PCR no es automáticamente equivalente a la variante por VSG; la fórmula, las unidades y los puntos de corte deben corresponder a la fuente y la edición utilizadas.

## Referencias

- [Prevoo MLL et al. Modified disease activity scores that include twenty-eight-joint counts: development and validation in a prospective longitudinal study of patients with rheumatoid arthritis. Arthritis Rheum, 1995.](https://doi.org/10.1002/art.1780380107)

- [Wells G et al. Validation of the 28-joint Disease Activity Score (DAS28) and European League Against Rheumatism response criteria based on C-reactive protein against disease progression in patients with rheumatoid arthritis, and comparison with the DAS28 based on erythrocyte sedimentation rate. Ann Rheum Dis, 2009.](https://doi.org/10.1136/ard.2007.084459)

- [England BR et al. 2019 Update of the American College of Rheumatology Recommended Rheumatoid Arthritis Disease Activity Measures. Arthritis Care Res, 2019.](https://doi.org/10.1002/acr.24042)

## Reproducir las pruebas técnicas

Ejecute node test.cjs en el directorio raíz de este repositorio para repetir los casos sintéticos registrados. Se conservan las entradas, los resultados esperados y las tolerancias originales. Las pruebas técnicas no constituyen validación clínica.

```sh
node test.cjs
```

tool.json contiene las fuentes, la edición y el alcance de la revisión. examples.json conserva las entradas y los resultados esperados de los casos sintéticos; results.json registra los resultados obtenidos.

[Ficha y referencias](../tool.json) · [Código JavaScript](../calculator.js) · [Casos de referencia](../examples.json) · [results.json](../results.json)

## Revisión y condiciones de uso

No se ha realizado una revisión clínica independiente.

Esta interfaz es una traducción de elaboración propia, no una edición oficial o certificada. No se han realizado la revisión clínica independiente, la revisión lingüística profesional ni la autorización de derechos de los instrumentos.

Resultado de la fórmula o clasificación. La interpretación, la conducta y la aplicabilidad dependen de la evaluación profesional y de la fuente seleccionada.

## Licencia y atribución

Apache-2.0 se aplica únicamente al código de ELUCENIA. Los derechos de los instrumentos, publicaciones, traducciones y datos permanecen en manos de sus respectivos titulares. Conserve LICENSE y NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026
