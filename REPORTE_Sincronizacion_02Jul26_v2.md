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

---

# Ronda 2 · Ajuste al índice de la presentación (IndicePresentacionDirectores_02Jul26_v1) y a la propuesta v3 final

## 5. Reestructuración al índice

El índice define el flujo: **01 Resumen ejecutivo → 02 Contexto → 03 Oportunidad (cuadrante + prioridades + focos) → 04 Solución → 05 Roadmap**. La única sección fuera de ese orden era `#valor` (solución), que aparecía antes del bloque de oportunidad.

| # | Cambio | Detalle | Motivo / fuente |
|---|--------|---------|-----------------|
| 6 | **Orden de secciones** | `#valor` se movió de la posición 4 (entre `#hoy` y `#mapa`) a después de `#foco3` (antes de `#agentes`) | Índice: la Solución (04) va después de la Oportunidad (03). Nuevo orden: destino · bien · hoy · mapa · top3 · foco1-3 · **valor** · agentes · difer · talento · plan · decision |
| 7 | Eyebrow de `#mapa` | "El resto, de un vistazo · 26 oportunidades" → "**La oportunidad**, de un vistazo · 26 oportunidades" | Al mover `#valor`, el mapa ya no viene "después" de nada que justifique "el resto"; abre el bloque 03 · Oportunidad del índice |
| 8 | Eyebrow de `#valor` | "La propuesta de valor" → "**La solución · La plataforma que proponemos**" | Índice 04 · Solución; propuesta v3 sección 06 |
| 9 | Cierre de `#valor` (nuevo párrafo) | Se agregó el puente prioridades→fases: "Así se implementan las tres prioridades a lo largo de las fases: cierre y conciliación arranca en la Fase 1… culmina en la Fase 3 con el orquestador…; cuentas por pagar… Fases 1–2…; garantías… Fases 2–3…" | Nota del índice en 04: "explicar de las prioridades cómo irlas implementando en las fases". Fases tomadas de la propuesta v3 (secciones 05, 07 y 10) |
| 10 | `#plan` · chips Fase 1 | Se agregó el chip "**Cuentas por pagar · viáticos**" | Roadmap v3, Fase 1: "Capa de datos · conciliación · **cuentas por pagar · viáticos** · tablero v1 · piloto" — faltaban en los chips |
| 11 | `#plan` · chips Fase 2 | Se agregó el chip "**Contabilidad entre empresas · plan de piso e inventario**" | Roadmap v3, Fase 2: "…contabilidad entre empresas · **plan de piso e inventario**…" — no estaban en la Fase 2 del HTML |
| 12 | `#plan` · chips Fase 4 | Se eliminó el chip "Plan de piso e inventario consolidado" | **Corrección de fase:** la propuesta v3 (roadmap y OPS O11/O12/O14) ubica plan de piso e inventario en la **Fase 2**, no en la Fase 4. La Fase 4 queda como en la v3: nómina y RH · calibración final · entrega formal |

Mapeo final secciones ↔ índice: **01 Resumen** = destino · **02 Contexto** = bien + hoy · **03 Oportunidad** = mapa + top3 + foco1-3 · **04 Solución** = valor + agentes + difer + talento · **05 Roadmap** = plan · Cierre = decision.

No se agregaron a la presentación las secciones de la propuesta que no van a pantalla para directores (equipo/metodología, plazos detallados, inversión, ROI, términos comerciales): el índice de la presentación solo cubre 01–05 y la inversión/ROI la presenta Mauricio por separado (regla vigente de la ronda 1).

## 6. Verificaciones de la ronda 2 — todas pasaron

| Verificación | Resultado |
|--------------|-----------|
| `node --check` sobre el bloque `<script>` | ✓ OK |
| `const OPS`: 26 objetos · rapido=8 · apuesta=7 · incremental=9 · diferir=2 | ✓ Intacto (no se tocó) |
| Regresiones: "olas", "58 personas", "58 colaboradores", "800–1,000", eyebrows viejos, plan de piso en Fase 4 | ✓ 0 coincidencias en todos |
| Cadenas nuevas presentes exactamente 1 vez (8 cadenas) | ✓ 8/8 |
| Protegidos: "$58.8M", geometría del scatter, base64 | ✓ Intactos (el movimiento de `#valor` fue byte-exacto: mismo tamaño de archivo antes/después del corte-pega) |
| Render Chromium headless | ✓ 0 errores JS · 14 secciones en el nuevo orden · scatter con 26 burbujas · gantt con 4 fases y 4 tarjetas de fase completas |

*Nota sobre las capturas automatizadas: los huecos en blanco y la "línea" sobre el título que se veían en screenshots intermedios eran artefactos de captura (animaciones `.reveal` sin disparar y la barra de progreso fija del nav); en el navegador la página se muestra completa.*
