# Entrenamiento Resto Druid PvP — Midnight

Sistema personal de entrenamiento PvP para un **Druida Restauración** (Keeper of the Grove, Alianza–DunModr). No es un proyecto de código: son documentos vivos de coaching, organizados en fases con métricas medibles.

**Parche actual:** 12.1, Midnight Season 2 · **Última revalidación:** 2026-09-12 · **24 documentos**

---

## 👉 Por dónde empezar

### **[`01-plan/ruta_de_trabajo.md`](01-plan/ruta_de_trabajo.md) — empieza aquí**

Es la ruta paso a paso de todo el proyecto: qué ya está hecho, qué toca ahora y en qué orden sigue. Si te pierdes entre los 23 documentos, vuelve a ese archivo.

**Si prefieres leer primero la base (30 min):**

1. **[`00-perfil/perfil_jugador.md`](00-perfil/perfil_jugador.md)** — quién eres: ratings, gear, debilidades declaradas
2. **[`00-perfil/glosario_conceptos.md`](00-perfil/glosario_conceptos.md)** — qué es DR, tipos de CC, target vs focus
3. **[`03-talentos/kit_resto_druid.md`](03-talentos/kit_resto_druid.md)** — qué hace cada hechizo de tu spec
4. **[`01-plan/roadmap_fases.md`](01-plan/roadmap_fases.md)** — el plan completo en 5 fases

> Los tres primeros son la base. El resto del proyecto los da por sabidos.

---

## Estado actual

| Fase | Estado |
|---|---|
| **0 — Cimientos técnicos** | ✅ Completada (2026-09-12) |
| **1 — Sanación bajo presión** | ⏳ Siguiente |
| 2 — Juego ofensivo ⭐ | Pendiente |
| 3 — Equipo y comunicación | Pendiente |
| 4 — Push sostenido | Pendiente |

**Pendiente inmediato:** construir el hábito de *mouse turning* (práctica, no configuración).

**Compromiso abierto:** rellenar el [registro de temporada](04-seguimiento/registro_temporada.md) desde la primera sesión. Es el único documento que solo se llena jugando, y alimenta todo el análisis de Fase 4.

---

## Mapa de documentos

### 00 — Perfil y referencia

| Archivo | Qué es |
|---|---|
| [`perfil_jugador.md`](00-perfil/perfil_jugador.md) | Ratings, gear, autodiagnóstico, preferencias de coaching |
| [`glosario_conceptos.md`](00-perfil/glosario_conceptos.md) | DR, tipos de CC, target vs focus, siglas, elementos de la UI |
| [`fuentes.md`](00-perfil/fuentes.md) | Todas las fuentes del proyecto y cuándo caduca cada una |

### 01 — Plan de entrenamiento

| Archivo | Qué es |
|---|---|
| [`ruta_de_trabajo.md`](01-plan/ruta_de_trabajo.md) | **👉 Empieza aquí.** Ruta paso a paso: lo hecho, lo de ahora y lo que sigue |
| [`roadmap_fases.md`](01-plan/roadmap_fases.md) | **La columna vertebral.** Las 5 fases con métricas de salida |
| [`fase1_sanacion_bajo_presion.md`](01-plan/fase1_sanacion_bajo_presion.md) | 3 modos de sanación, capas defensivas, guerra de maná |
| [`fase2_juego_ofensivo.md`](01-plan/fase2_juego_ofensivo.md) | DR, Cyclone, fake casting, posicionamiento anti-CC |
| [`fase3_equipo_comunicacion.md`](01-plan/fase3_equipo_comunicacion.md) | Comps, cómo encontrar equipo, protocolo de voz |
| [`fase4_push_sostenido.md`](01-plan/fase4_push_sostenido.md) | VODs, proporción 75/25, gestión mental |
| [`guia_blitz.md`](01-plan/guia_blitz.md) | Battleground Blitz: build propio, rol, addons |
| [`guia_mapas_bg.md`](01-plan/guia_mapas_bg.md) | Los 9 mapas del pool: cómo se gana cada uno |
| [`guia_revalidacion_s2.md`](01-plan/guia_revalidacion_s2.md) | Protocolo para actualizar todo tras un parche |

### 02 — Configuración

| Archivo | Qué es |
|---|---|
| [`macros_y_ui.md`](02-configuracion/macros_y_ui.md) | **Tu configuración REAL**: keybinds, addons instalados, plan de migración |
| [`macros_resto_druid.md`](02-configuracion/macros_resto_druid.md) | Las macros con código en español + glosario EN→ES |
| [`addons_ui_programas.md`](02-configuracion/addons_ui_programas.md) | Stack de addons y configuración de la UI base |
| [`resumen_addons.md`](02-configuracion/resumen_addons.md) | Tabla rápida de addons con prioridades |
| [`gear_gemas_enchants.md`](02-configuracion/gear_gemas_enchants.md) | Gemas, enchants, embellishments, tier set, stats por bracket |

### 03 — Talentos y clase

| Archivo | Qué es |
|---|---|
| [`kit_resto_druid.md`](03-talentos/kit_resto_druid.md) | **Qué hace cada hechizo.** Referencia base de la clase |
| [`talentos_core.md`](03-talentos/talentos_core.md) | Los 12 talentos que requieren decisión activa |
| [`talentos_flexibles.md`](03-talentos/talentos_flexibles.md) | Swaps por matchup |
| [`matchups.md`](03-talentos/matchups.md) | Cómo jugar contra cada clase enemiga |

### 04 — Seguimiento

| Archivo | Qué es |
|---|---|
| [`registro_temporada.md`](04-seguimiento/registro_temporada.md) | **Log de sesiones.** El motor del análisis de patrones |

---

## Reglas del proyecto

1. **El tooltip in-game gana** sobre cualquier tabla de estos archivos.
2. **Dato vivo (Murlok.io) gana sobre recomendación editorial** (Icy Veins) cuando choquen.
3. **Cliente en español:** las macros llevan los nombres de hechizo en español o no funcionan. Método: **Shift+clic**.
4. **Datos de meta caducan con cada parche.** Consejo situacional (regla de trinket, decisiones de Cyclone, comunicación) no caduca.
5. **Resto NO tiene Mighty Bash en Midnight.** El stun es Rake desde Prowl y Maim (Amputar).

---

## Cómo se usa este sistema

**En Claude Code (este repo):** investigación de meta, actualización de documentos, revalidación tras parches, configuración.

**En la app de escritorio:** coaching post-partida, dudas de juego, análisis de sesiones.

> El repo es la fuente de verdad. Lo que se decida en la app y deba persistir, se trae aquí.

**Tras cada parche mayor:** ejecutar [`guia_revalidacion_s2.md`](01-plan/guia_revalidacion_s2.md).
