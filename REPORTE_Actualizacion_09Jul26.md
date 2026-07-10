# Actualización a los entregables finales del 9 de julio · Presentación de Directores Cabina
## Grupo Dicas · Confidencial DaCodes

> **⭐ VERSIÓN FINAL RECOMENDADA: `Cabina_Presentación_Discovery_09Jul26_V2.html`**
>
> Tras revisar, la Verónica indicó que su landing más reciente (`PresentaciónDiscovery03Jul26_V1`) **ya incluía un mapa de procesos interactivo** (overlay a pantalla completa con filtros Mapa/Lista · Ciclo de cierre · Ciclo de pagos · etc.), que se perdía con el anexo de imágenes estáticas de la Versión B.
>
> **Corrección:** tomé **su archivo con el mapa interactivo como base** y le apliqué solo las 4 actualizaciones de información del 9-jul (piloto, SAT 32-D, garantías por confirmar, fecha/fuente). El mapa interactivo queda **100% intacto** (está embebido como blob HTML en base64 dentro del archivo y no se tocó). Esta `..._V2.html` **sustituye** a las versiones A (solo datos) y B (imágenes estáticas) de abajo, que quedan como referencia del análisis.
>
> Verificado: los 3 bloques `<script>` pasan `node --check`; `const OPS` intacto (26, 8/7/9/2); cero "olas"; las 4 actualizaciones presentes; el mapa embebido conserva "Ciclo de cierre/pagos", toggle "Mapa/Lista" y los 22 nodos.

---


**Fecha:** 9 de julio de 2026
**Fuente de verdad:** Entregables finales del Discovery (Google Drive), leídos íntegros:
- **E1** — Mapa Visual de Procesos, **22 fichas V5 del 9-jul** (P1–P22), cada una con su diagrama §5 regenerado con la convención visual del deck.
- **E2** — Catálogo Priorizado de Oportunidades v7 (9-jul) · **E3** Validación de Prototipo v4 · **E4** Propuesta de Desarrollo Formal v5 · **E5** Hoja de Ruta v5.

**Base:** `Cabina_Presentación_Directores_02Jul26_v2.html` (ya sincronizada a la propuesta v3, con logos y orden por índice).

## Dos versiones entregadas
| Archivo | Qué es |
|---|---|
| `Cabina_Presentación_Directores_09Jul26_vA_datos.html` | **Versión A** — solo sincronización de información. Formato/branding/funcionalidad intactos; sin diagramas de proceso. (~0.9 MB) |
| `Cabina_Presentación_Directores_09Jul26_vB_diagramas.html` | **Versión B** — igual que A **+ los diagramas del E1**: los 3 de las prioridades insertados en sus focos y un anexo con los 22. (~2.3 MB, autocontenido) |

---

## 1. Cambios de información (aplicados a AMBAS versiones)

| # | Ubicación | Cambio | Fuente (9-jul) |
|---|-----------|--------|----------------|
| 1 | #top3 Prioridad 1 · #foco1 | Se agregó la **validación de directores del 3-jul**: cierre + conciliación es **el piloto** — una empresa, ~6 meses, meta de cierre <2 días | E1 P1/P3 (fila "Validación ejecutiva"), E2 §7, E4 §2, E5 |
| 2 | #top3 Prioridad 2 | Se agregó: **verificar la opinión de cumplimiento del SAT (32-D)** del proveedor antes de pagar | E1 P4/P18 (petición de Paola Padilla, 3-jul) |
| 3 | #top3 Prioridad 3 · #foco3 | Garantías marcada como **"Prioridad por confirmar con la Dirección"** | E1 P9 + E2/E4: O9 cuestionada por Alejandra Estrada el 3-jul; queda condicionada |
| 4 | Pie de página | Fuente → "etapas 1 a 5 · entregables finales E1–E5 (v5) · **9 de julio de 2026**" | Fecha de los entregables finales |

**Cifras cotejadas y ya correctas (sin cambio):** 59 admón. central (E4 confirma vs vieja hipótesis ~30) · 671 división / 1,036 corporativo / 83 central compartida · 56 cuentas (39 Banorte) · ≈1,000 facturas/mes · ~600 cheques · cierre 5–6 días→<2 · garantías $35–55K GM, ~$50K/año, 300–500 reclamos/mes · $6M Premier (error ~$200K) · PLD 3–4 días/mes (proceso completo) · $58.8M refacciones (confirmado "no urgente") · 658 unidades · 26 oportunidades · 22 procesos · 12 meses en 4 fases (Cimientos/Expansión/Madurez/Optimización) · terminología "fases" (los 4 entregables migraron de "olas"→"fases").

---

## 2. Diagramas del E1 (solo Versión B)

Se extrajeron los **22 diagramas de flujo §5** de los Docs V5 (export PDF → imagen), se redujeron a 1200 px y se optimizaron a PNG de paleta (128 colores) — el texto queda nítido y el total pesa ~1.2 MB en base64. Colocación:

- **En los 3 focos:** el diagrama de su proceso prioritario — Foco 1 → PROC-01 Cierre; Foco 2 → PROC-04 Cuentas por Pagar; Foco 3 → PROC-09 Garantías.
- **Anexo nuevo "Estado actual, proceso por proceso" (id `#diagramas`)**, insertado antes del cierre: los **22 procesos** (PROC-01…22) con su nombre y diagrama, en una sola columna.

Los diagramas ya vienen con la convención visual del deck (fricción en coral, revisiones que disparan reproceso en violeta), así que se integran sin romper el branding. Ninguna otra sección, estilo ni interactividad se modificó.

---

## 3. Delta detectado NO aplicado (requiere tu confirmación)

**Distribución de cuadrantes del mapa.** La presentación tiene **8 rápidas / 7 apuestas / 9 incrementales / 2 diferir**. El **E2 v7** reporta **8 / 8 / 8 / 2** (una oportunidad más en "apuestas grandes", una menos en "incrementales"). **No modifiqué el array `OPS`** por dos razones:
1. La lista secundaria de membresía por cuadrante que se extrajo del E2 reclasificaba O1 (la victoria rápida insignia, impacto 5 / esfuerzo 3) como "apuesta grande", lo que es casi seguro un error de transcripción — mover burbujas con datos dudosos arriesga corromper el scatter verificado.
2. La instrucción vigente sobre `OPS` es "si detectas discrepancia, repórtala, no la edites".

**Acción sugerida:** confirmar contra el E2 v7 **cuál** oportunidad puntual cambió de incrementales a apuestas grandes; con ese dato hago el ajuste de una sola burbuja con seguridad.

---

## 4. Otras observaciones de los entregables (informativas)

- **"11 agentes":** el E4 aclara que la **Fase 1 son 6 módulos/agentes** (M1–M6); "11" es el total del proyecto. La presentación ya no afirma un número de agentes (esa sección se retiró antes), así que no hubo nada que corregir.
- **18 puntos / 3 estados:** no aparecen en E2–E5 (el E3 usa "12 agencias" como ejemplo), pero sí están en la propuesta formal y en E1; se conservan.
- **Reportes OEM (P10) y refacciones obsoletas (P8):** los directores los marcaron "no urgentes"; no figuran como prioridad en el deck, coherente.
- **E3 · prototipo:** contiene cifras del prototipo que contradicen las validadas (AR ~64% vencida vs ~5% real; nómina 650 vs 671). Son datos internos del prototipo a reetiquetar, no de esta presentación — pero ojo si algún material reusa capturas del prototipo.

---

## 5. Verificaciones (ambas versiones)

| Verificación | A | B |
|---|---|---|
| `node --check` del `<script>` | ✓ OK | ✓ OK |
| `const OPS`: 26 objetos · 8/7/9/2 | ✓ (intacto) | ✓ (intacto) |
| Regresión "olas" | ✓ 0 | ✓ 0 |
| Textos nuevos (piloto, 32-D, garantías por confirmar, fecha 9-jul) presentes | ✓ | ✓ |
| Imágenes (`<img>`) | 1 (logo) | 26 (logo + 3 focos + 22 anexo) |
| Render Chromium: secciones, scatter 26 burbujas, imágenes cargadas, 0 errores JS | ✓ 11 secciones | ✓ 12 secciones · 22+3 diagramas · naturalWidth OK · 0 errores |
