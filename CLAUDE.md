# Proyecto: Entrenamiento Resto Druid PvP — Midnight

Sistema personal de entrenamiento PvP (arenas 3v3 y RBG) para un Druida Restauración, Keeper of the Grove, Alianza-DunModr. No es un proyecto de código: son documentos vivos de coaching.

## Contexto obligatorio

- **Lee siempre `perfil_jugador.md` primero** — es el contexto base de cualquier respuesta (ratings, debilidades declaradas, disponibilidad de 8 h/semana, preferencias de coaching).
- Si un dato marcado `[COMPLETAR]` es relevante para la respuesta, pídelo antes de responder.
- Parche actual: **12.0.7, Midnight Season 1**. Season 2 llega con 12.1 a mediados de agosto de 2026 y cambia builds, Innervate, DR (16→20 seg) y tuning. Cada archivo marca qué le caduca.

## Mapa de archivos

| Archivo | Qué es | Regla de uso |
|---|---|---|
| `perfil_jugador.md` | Quién es el jugador, ratings, autodiagnóstico | Contexto base en todos los chats |
| `roadmap_fases.md` | Plan de entrenamiento en 5 fases (0-4) con métricas de salida | La columna vertebral; sincronizado 2026-07-12 con los archivos de detalle |
| `macros_resto_druid.md` | Las 11 macros obligatorias + opcionales, keybinds, drill | Fuente de verdad de macros (detalle de Fase 0.3) |
| `addons_ui_programas.md` | UI base + stack de addons post-"Addon Apocalypse" | Fuente de verdad de addons (detalle de Fase 0.2) |
| `talentos_core.md` | Los 12 talentos 48-50/50 que requieren decisión activa | Referencia estable dentro de S1 |
| `talentos_flexibles.md` | Talentos de swap por matchup (zona media del heatmap) | Material de Fase 4; no forzar en Fases 0-1 |
| `macros_y_ui.md` | Configuración ACTUAL del jugador | Refleja estado real; sugerir cambios incrementales desde lo que hay, no ideales desde cero |
| `registro_temporada.md` | Log de sesiones y resúmenes semanales | En el chat de Tracking: registrar sesiones en su formato y señalar patrones cada 2-3 semanas |

## Reglas de precedencia

1. **El tooltip in-game gana** sobre cualquier tabla de estos archivos (Midnight rediseñó parte del kit).
2. Los archivos de detalle (`macros_resto_druid.md`, `addons_ui_programas.md`) ganan sobre los resúmenes del roadmap si llegaran a divergir.
3. Datos de meta (builds, stats, comps, win rates) caducan con parches → revalidar en Murlok.io/Icy Veins antes de S2. Consejo situacional (regla de trinket, árbol de decisión de Cyclone, protocolo de comunicación) es estable.
4. **Resto NO tiene Mighty Bash en Midnight.** El stun es Rake desde Prowl (fuera de combate) y Maim (en combate). WeakAuras está muerto en retail; no recomendarlo.

## Estado actual (actualizar al avanzar)

- **Fase actual: 0 (Cimientos técnicos)** — sin addons ni macros instalados aún.
- **El jugador es clicker, en proceso de migración a keybinds** (declarado 2026-07-12). Las habilidades de reacción deben migrar a teclas ANTES de cerrar Fase 0 / empezar Fase 1.
- Pendiente en `macros_y_ui.md`: esquema de teclas actual, estilo de movimiento, teclas incómodas.
- `registro_temporada.md` sin sesiones registradas todavía.
- Datos relevantes del jugador: latencia 192-201 ms (Bogotá), 58 FPS en team fights, mouse con 2 botones laterales, dispel en scroll abajo.

## Estilo de coaching (declarado por el jugador)

- Análisis directo y honesto, sin validación vacía.
- Planes por fases con métricas medibles (estilo entrenamiento de gimnasio).
- Terminología de spells/mecánicas en inglés, explicación en español.
- Respuestas concisas y accionables.
