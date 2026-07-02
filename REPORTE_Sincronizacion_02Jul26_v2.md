# Reporte de sincronización · Presentación HTML de Directores v2
## Proyecto Cabina · Grupo Dicas · Confidencial DaCodes

**Fecha:** 2 de julio de 2026
**Fuente de verdad:** `Cabina_Propuesta_Formal_02Jul26_v3` (Google Docs, cifras cotejadas contra la hoja de validación del cliente)
**Destino:** `Cabina_Presentación_Directores_02Jul26_v2.html` (derivado de la v1 adjunta, sin cambios de diseño, estructura ni interactividad)

---

## 1. Cambios aplicados

| # | Ubicación | Texto anterior | Texto nuevo | Motivo / fuente |
|---|-----------|----------------|-------------|-----------------|
| 1 | `#bien` · tarjeta "Un equipo que lo sostiene a mano" | 58 personas del corporativo unen los sistemas manualmente | **59 personas de la administración central** unen los sistemas manualmente | Cifra validada (hoja de validación; propuesta formal, secciones 01 y 02) |
| 2 | `#hoy` · dato destacado del motor humano | 58 \<small\>colaboradores corporativos — el motor humano del grupo\</small\> | **59** \<small\>**colaboradores de administración central** — el motor humano del grupo\</small\> | Cifra validada: 59 colaboradores de administración central (propuesta formal, resumen ejecutivo) |
| 3 | `#foco2` · panel "Transmisión manual", cifra grande | 800–1,000 (Facturas recibidas al mes) | **≈1,000** (Facturas recibidas al mes) | Promedio confirmado en hoja de validación: "alrededor de 1,000 facturas de proveedor recibidas al mes" (propuesta formal, sección 02) |
| 4 | `#foco3` · panel "Transmisión manual", lista | *(no se mencionaba volumen)* | Se agregó el ítem **"300–500 reclamos al mes"** (tras "Por reclamo rechazado (GM)") | Volumen confirmado en hoja de validación: "garantías… 300–500 reclamos al mes" (propuesta formal, sección 02 y anexo de trazabilidad) |
| 5 | `#top3` · prioridad 01, stat de caso Premier | \<span class="n"\>$6 millones\</span\>\<span class="t"\>sin identificar **a tiempo** (caso Premier)\</span\> | \<span class="n"\>**hasta** $6 millones\</span\>\<span class="t"\>sin identificar **de inmediato** (caso Premier)\</span\> | Framing validado: "hasta $6M sin identificar de inmediato" — pico temporal, nunca pérdida recurrente (anexo de trazabilidad de la propuesta) |

**Corrección obligatoria #5 (PLD "3–4 días/mes" → precisar "(proceso completo)"):** la frase **no aparece** en el HTML fuera del array `OPS`. Ver discrepancias reportadas abajo (O20).

---

## 2. Discrepancias detectadas en `const OPS` — NO editadas (se reportan)

Por instrucción, el array `OPS` no se modificó. Se detectaron estas diferencias contra la propuesta formal:

| ID | Campo | Texto actual en OPS | Dato en la propuesta formal |
|----|-------|--------------------|-----------------------------|
| O3 | `d` | "Entre 800 y 1,000 facturas recibidas al mes" | "Alrededor de 1,000 facturas recibidas al mes" (≈1,000, promedio confirmado) |
| O9 | `d` | "cientos de reclamos al mes (sin consolidar)" | Volumen ya confirmado: **300–500 reclamos al mes** (ya no está "sin consolidar") |
| O20 | `d` | "liberar 3 a 4 días al mes" | "3–4 días al mes **(proceso completo**, de la gestión con el cliente al dictamen**)**" |

*Nota: O1 en OPS ya usa el framing correcto del caso Premier ("hasta 6 millones de pesos sin identificar de inmediato") — sin cambios.*

---

## 3. Cotejo sección a sección (sin cambios adicionales)

| Sección HTML | Equivalente en propuesta | Resultado |
|--------------|--------------------------|-----------|
| `#bien` | "El grupo ya hace bien lo difícil" | ✓ Coincide (18 puntos, 6 marcas, 3 estados; Stellantis día 7, GM día 13). Corrección #1 aplicada. |
| `#hoy` | "La administración hoy" | ✓ Coincide. Corrección #2 aplicada. "Ya pasó un mes" se conserva como redacción de pantalla del rezago de 30–45 días (cifra aún "por validar como dato duro" en la propuesta). |
| `#valor` | "Propuesta de valor" | ✓ Coincide (cierre 5–6 días → menos de 2; préstamos entre empresas como raíz). |
| `#mapa` | Sección 05 · 26 oportunidades | ✓ Coincide, incluida la nota "Ojo al leer el mapa". |
| `#top3` | "Tres prioridades" | ✓ Composición por oportunidades idéntica (O1·O6·O5·O15·O13 / O3·O4·O24·O25 / O9·O10). Corrección #6 aplicada. ~$50 mil/año y $35–55K por reclamo coinciden. |
| `#foco1` | Foco cierre/conciliación | ✓ Coincide (5–6 días, 56 cuentas, módulo descompuesto, <2 días). |
| `#foco2` | Foco cuentas por pagar | ✓ Corrección #3 aplicada; ~600 cheques coincide con promedio confirmado. |
| `#foco3` | Foco garantías | ✓ Corrección #4 aplicada (volumen 300–500/mes). |
| `#agentes` | Sección 06 (once agentes) | ✓ Coincide (11 agentes + capa de datos). |
| `#difer` | "Convivir, no sustituir" | ✓ Coincide (solo lectura, Business Pro sigue siendo fuente de verdad). |
| `#talento` | Nota honesta / framing de liberación | ✓ Framing correcto (liberación de tiempo, no recorte). El 70/30 → 90/10 se conserva: el propio HTML lo marca como "cifras ilustrativas del diagnóstico — no un dato medido"; la propuesta no lo contradice (el 41% de la propuesta mide otra cosa: tiempo en preparar/copiar datos). |
| `#plan` | "Roadmap 12 meses / 4 fases" | ✓ Coincide (4 fases, contenidos por fase, hito ejecutivo del mes 4). Terminología "fases" en todo el documento. |
| `#decision` | Próximos pasos | ✓ Coincide. Sin precios, inversión ni ROI en el HTML. |

**Protegidos y verificados intactos:** "$58.8M / 58.8 millones" (inventario de refacciones, en OPS O14), constantes de geometría del scatter (`b:58`, etc.), fuentes embebidas en base64 (el archivo no se reformateó; solo 5 reemplazos puntuales de coincidencia única).

---

## 4. Verificaciones pasadas

| Verificación | Resultado |
|--------------|-----------|
| `node --check` sobre el único bloque `<script>` extraído | ✓ Sintaxis OK |
| `const OPS` con exactamente 26 objetos | ✓ 26 |
| Conteos por cuadrante | ✓ rapido=8 · apuesta=7 · incremental=9 · diferir=2 |
| Grep de regresión: "olas" (palabra completa, excluyendo base64) | ✓ 0 coincidencias |
| Grep de regresión: "58 personas" | ✓ 0 coincidencias |
| Grep de regresión: "58 colaboradores" | ✓ 0 coincidencias |
| Grep de regresión: "800–1,000" (y variante con guion) | ✓ 0 coincidencias |
| Nuevos textos presentes exactamente 1 vez cada uno | ✓ 5/5 |
| Render en Chromium headless (Playwright) | ✓ 0 errores JS/consola · 14 secciones · scatter con las 26 burbujas (8 verdes, 7 moradas, 9 grises, 2 naranjas) · secciones editadas verificadas visualmente por captura |
| Peso del archivo | 925,043 bytes (v1: 924,974) — sin reformateo, solo los 5 reemplazos puntuales |
