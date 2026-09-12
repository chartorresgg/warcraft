# Proyecto: Entrenamiento Resto Druid PvP — Midnight

Sistema personal de entrenamiento PvP (arenas 3v3 y RBG) para un Druida Restauración, Keeper of the Grove, Alianza-DunModr. No es un proyecto de código: son documentos vivos de coaching.

## Contexto obligatorio

- **Lee siempre `00-perfil/perfil_jugador.md` primero** — es el contexto base de cualquier respuesta (ratings, debilidades declaradas, disponibilidad de 8 h/semana, preferencias de coaching).
- Si un dato marcado `[COMPLETAR]` es relevante para la respuesta, pídelo antes de responder.
- Parche actual: **12.1, Midnight Season 2** (parche 11 ago 2026; temporada desde el 18 ago). Revalidado el 2026-09-11 contra Murlok.io, Icy Veins y los hotfixes del 1 de septiembre.
- **El cliente del jugador está en español (esES).** Dos consecuencias:
  1. **Macros:** los **nombres de hechizo van en español** (los comandos `/cast`, `/use`, `#showtooltip` siguen en inglés) o la macro no funciona — falla en silencio. Glosario EN→ES en `02-configuracion/macros_resto_druid.md`. Método siempre: **Shift+clic** sobre el hechizo, por el fallo de acentos del cliente español.
  2. **Nombres en general:** spells, talentos, runas y **opciones de menú del juego** se escriben en **inglés con el español entre paréntesis** — ej. *Cyclone (Ciclón)*, *Nameplates (Placas de nombre)*. El inglés es el de las guías (Murlok, Icy Veins, Skill Capped); el español es lo que el jugador ve en pantalla. Aplica a TODOS los archivos, no solo a los de macros.

## Mapa de archivos

| Archivo | Qué es | Regla de uso |
|---|---|---|
| `00-perfil/perfil_jugador.md` | Quién es el jugador, ratings, autodiagnóstico | Contexto base en todos los chats |
| `00-perfil/glosario_conceptos.md` | DR, tipos de CC, vocabulario de arena, siglas, elementos de la UI | El jugador es nuevo en la terminología. **No asumas conceptos: si usas uno que no está aquí, explícalo en una línea y añádelo** |
| `01-plan/roadmap_fases.md` | Plan de entrenamiento en 5 fases (0-4) con métricas de salida | La columna vertebral; recalendarizado 2026-09-11 a S2 |
| `01-plan/fase1_sanacion_bajo_presion.md` | Detalle de Fase 1: 3 modos de sanación, capas defensivas, guerra de maná en S2 | Fuente de verdad de Fase 1 (creado 2026-09-11) |
| `01-plan/fase2_juego_ofensivo.md` | Detalle de Fase 2: DR, Cyclone, fake casting, posicionamiento anti-CC | Fuente de verdad de Fase 2 |
| `01-plan/fase3_equipo_comunicacion.md` | Detalle de Fase 3: comps de S2, cómo encontrar equipo, protocolo de voz, el go coordinado | Fuente de verdad de Fase 3 (creado 2026-09-12). **No se entrena en Shuffle** |
| `01-plan/fase4_push_sostenido.md` | Detalle de Fase 4: VODs, proporción 75/25, gestión mental, ciclo semanal, RBG/Blitz | Fuente de verdad de Fase 4 (creado 2026-09-12). No termina: es modo de operación permanente |
| `01-plan/guia_revalidacion_s2.md` | Protocolo de revalidación tras un parche mayor | Ejecutado el 2026-09-11 para 12.1; reutilizable en el próximo parche |
| `02-configuracion/gear_gemas_enchants.md` | Gemas, encantamientos, embellishments, trinkets, tier set y stats por bracket | Datos de meta: caducan con el parche. Revalidar en Murlok |
| `03-talentos/matchups.md` | Desglose por clase enemiga: cómo te matan, qué trinketear, posicionamiento | Material de Fase 3-4. Win rates de S2; la táctica es estable entre parches |
| `02-configuracion/macros_resto_druid.md` | Las 11 macros obligatorias + opcionales, **glosario EN→ES**, keybinds, drill | Fuente de verdad de macros (detalle de Fase 0.3). **Macros en español** |
| `02-configuracion/addons_ui_programas.md` | UI base + stack de addons post-"Addon Apocalypse" | Fuente de verdad de addons (detalle de Fase 0.2) |
| `02-configuracion/resumen_addons.md` | Tabla resumen de addons con prioridades | Vista rápida; si diverge, gana `addons_ui_programas.md` |
| `02-configuracion/macros_y_ui.md` | Configuración ACTUAL del jugador + plan de migración clicker→keybinds | Refleja estado real; sugerir cambios incrementales desde lo que hay, no ideales desde cero |
| `03-talentos/talentos_core.md` | Los 12 talentos 48-50/50 que requieren decisión activa | Revalidado en S2 (12.1) |
| `03-talentos/talentos_flexibles.md` | Talentos de swap por matchup (zona media del heatmap) | Material de Fase 4; no forzar en Fases 0-1 |
| `04-seguimiento/registro_temporada.md` | Log de sesiones y resúmenes semanales | En el chat de Tracking: registrar sesiones en su formato y señalar patrones cada 2-3 semanas |

## Reglas de precedencia

1. **El tooltip in-game gana** sobre cualquier tabla de estos archivos (Midnight rediseñó parte del kit).
2. Los archivos de detalle (`02-configuracion/macros_resto_druid.md`, `02-configuracion/addons_ui_programas.md`) ganan sobre los resúmenes del roadmap si llegaran a divergir.
3. Datos de meta (builds, stats, comps, win rates) caducan con parches → revalidar en Murlok.io/Icy Veins antes de S2. Consejo situacional (regla de trinket, árbol de decisión de Cyclone, protocolo de comunicación) es estable.
4. **Resto NO tiene Mighty Bash en Midnight.** El stun es Rake desde Prowl (fuera de combate) y **Maim = Amputar** (en combate). WeakAuras está muerto en retail; no recomendarlo.
5. **Antes de proponer una macro, verifica que el hechizo sea ACTIVO.** Midnight convirtió varias habilidades en pasivas y el proyecto arrastró consejos imposibles de ejecutar. Confirmados pasivos: **Grove Guardians** (los treants salen al castear Swiftmend o Wild Growth), **Flourish** (procea con Tranquility), **Efflorescence** en el build del jugador (por *Lifetreading*). Ante la duda, pregunta por el tooltip antes de escribir la macro.

## Estado actual (actualizar al avanzar)

- **Fase actual: 0 (Cimientos técnicos), prácticamente cerrada.** ✅ **0.2 addons** (2026-09-11) · ✅ **0.3 macros** (11 obligatorias + 6 opcionales, probadas in-game) · ✅ **0.4 keybinds** (2026-09-12): giro con teclado desbindeado y 10/12 binds implementados. **Ya NO es clicker en habilidades de reacción.** Pendiente menor: asignar Cyclone @arena1/2/3 a Shift+1/2/3, y **construir el hábito de mouse turning con práctica** (único bloqueo real restante).
- **Las curas base (1-5) siguen clickeadas a propósito** — son las de menor urgencia de reacción. No presionar para migrarlas.
- ⚠️ **Al dar una macro, escribe cada comando en su propia línea.** El formato de tabla de `macros_resto_druid.md` junta los comandos en una celda; pegarlos así rompe la macro (le pasó al jugador con las macros 4/5/6).
- ⚠️ **Maim = Amputar** (no "Destripar", que es Rip/sangrado). Error de traducción detectado y corregido el 2026-09-12.
- **Las macros de stun (7 y 7b) funcionan pero son material de Fase 2+.** Prowl exige estar fuera de combate; Amputar exige puntos de combo (= dejar de curar). No las fuerces en Fases 0-1.
- ⚠️ **El addon se llama MiniAuras, no "MiniCC".** El nombre "MiniCC" de los documentos de julio nunca se verificó contra la instalación real. Usa MiniAuras.
- **El jugador es nuevo en la terminología de PvP** (preguntó qué es DR tras cinco documentos usándolo). Ver `00-perfil/glosario_conceptos.md` y no asumir conceptos.
- **Ratings S2 (2026-09-11):** Solo Shuffle 1094 (328 rondas, 52% WR) · Battleground Blitz 1421 (52 partidas, 38% WR). La caída desde 1784/1670 es el reset de S2, no pérdida de nivel — el WR de Shuffle es positivo. **Blitz a 38% es el problema real.**
- **El jugador es clicker, en proceso de migración a keybinds** (declarado 2026-07-12). Todo clickeado: curas en 1-5, defensivos en barra 2. Las habilidades de reacción deben migrar a teclas ANTES de cerrar Fase 0 — plan incremental en `02-configuracion/macros_y_ui.md`.
- **Movimiento: W/S adelante-atrás, Q/E strafe, A/D giran (keyboard turning).** El paso 0 de la migración es girar con mouse y liberar A/D como teclas de habilidad. Q/E se conservan como strafe — NO sugerirlas para habilidades.
- `04-seguimiento/registro_temporada.md` sin sesiones registradas todavía.
- Datos relevantes del jugador: latencia 192-201 ms (Bogotá), 58 FPS en team fights, mouse con 2 botones laterales, dispel en scroll abajo, **cliente en español**.

## Estado del meta en S2 (revalidado 2026-09-11)

- **Confirmado sin cambios:** Keeper of the Grove (42/50), tríada Forest Guardian (50/50) + Early Spring (48/50) + Call of Ohn'ahra (35/50), Night Elf (50/50), stats de arena Mastery > Vers > Haste > Crit.
- **Cambió:** DR reset 16 → **20 seg** · Innervate rediseñado (**20% de maná en PvP**, no 25%) · nerfs del 1 de septiembre (Swiftmend −20%, Regrowth −20%, sanación general −5%, Incarnation acortado) · Typhoon slow 50% → 30% · Nature's Splendor eliminado · Overgrowth (25/50) y Flash of Clarity (0/50) nuevos · Abundance rediseñado.
- **Ancient of Lore regresó pero NO se juega (3/50)** — Icy Veins lo recomienda, el ladder lo ignora. No sugerir ese swap.
- **Stats difieren por bracket:** arena = Mastery primero; **Blitz/RBG = Versatility primero**.
- **Comp de mayor win rate del spec:** Resto Druid + Balance Druid + BM Hunter (77,5%).

## Estilo de coaching (declarado por el jugador)

- Análisis directo y honesto, sin validación vacía.
- Planes por fases con métricas medibles (estilo entrenamiento de gimnasio).
- Terminología de spells/mecánicas en inglés, explicación en español.
- Respuestas concisas y accionables.
