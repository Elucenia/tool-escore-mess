<!-- ELUCENIA technical documentation · escore-mess · es · no clinical/professional/rights approval -->

# MESS (puntuación de gravedad de extremidad gravemente lesionada)

[condiciones, fuentes y permisos](https://elucenia.org/es/herramientas/escore-mess)

## Cómo usar

Utilice la herramienta en el portal o abra index.html mediante un servidor HTTP local. Seleccione el idioma, complete los campos y calcule.

## Entradas y unidades

### Lesión esquelética y de partes blandas

`energia`

- `1` — Baja energía (herida por arma blanca, fractura simple, proyectil de arma corta)
- `2` — Energía media (fractura abierta o múltiple, luxación)
- `3` — Alta energía (accidente a alta velocidad, proyectil de fusil)
- `4` — Energía muy alta (lo anterior + contaminación intensa)

### Isquemia del miembro

`isquemia`

- `0` — Sin isquemia
- `1` — Pulso reducido o ausente, perfusión normal
- `2` — Sin pulso, parestesias, relleno capilar lento
- `3` — Miembro frío, paralizado e insensible

### ¿Isquemia desde hace más de 6 horas?

`tempo`

- `0` — No
- `1` — Sí

### Shock

`choque`

- `0` — Presión arterial sistólica siempre \> 90 mmHg
- `1` — Hipotensión transitoria
- `2` — Hipotensión persistente

### Edad

`idade`

- `0` — \< 30 años
- `1` — 30 a 50 años
- `2` — \> 50 años

## Edición del método

MESS/Johansen 1990: 4 dominios, isquemia duplicada \>6 h; sin orden automática de amputación

## Fórmula documentada

MESS = lesión esquelética/partes blandas (1 a 4) + isquemia (0 a 3, duplicada si dura más de 6 h) + shock (0 a 2) + edad (0 a 2).

## Límites y población

El MESS original se derivó en pequeños grupos con traumatismo grave de miembro inferior. La asociación del punto de corte ≥7 con amputación en esos grupos no establece una regla universal ni una indicación automática. La salvación del miembro depende de una evaluación multidisciplinar y de condiciones clínicas no resumidas en la puntuación.

## Referencias

- [Johansen K et al. Objective criteria accurately predict amputation following lower extremity trauma. J Trauma, 1990.](https://doi.org/10.1097/00005373-199005000-00007)

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
