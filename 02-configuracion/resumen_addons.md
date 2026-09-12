# Resumen de Addons — PvP Midnight (12.1)

> Verificado: 2026-07-12 · Revisado 2026-09-11 (sin cambios de stack en S2 — tras el parche: CurseForge → Update All → skirmish de verificación).
> Todos se instalan y auto-configuran con **Skill Capped UI** (CurseForge), salvo donde se indique. Todos los listados como 🔴/🟡 son gratuitos.

> 📌 **Sobre las prioridades:** esta tabla marca 🔴 los 6 perfiles que instala Skill Capped UI de una sola vez, porque no cuesta más marcarlos todos. El **núcleo imprescindible son 3** — sArena Reloaded, MiniAuras y FrameSort; BetterBlizzPlates, BetterBlizzFrames y Details son mejoras que vienen gratis en el mismo paquete. Si instalas manualmente, los 3 primeros son obligatorios y el resto opcional (así los clasifica `addons_ui_programas.md`, que es la fuente de verdad si hay divergencia).

| Addon | Categoría | Qué hace | Por qué te sirve a TI | Prioridad |
|---|---|---|---|---|
| **Skill Capped UI** | Instalador/configurador | Instala y aplica perfiles pre-configurados de todos los addons de abajo + ajustes ocultos (Spell Queue Window = latencia+100, cámara al máximo, sticky targeting, menos clutter visual) | Con tus ~200 ms, el Spell Queue en ~300 encadena tus hechizos sin micro-pausas. Te ahorra una tarde de configuración manual | 🔴 Instalar primero |
| **sArena Reloaded** | Frames de arena | Reemplaza los frames enemigos: barras con color de clase, cast bars grandes, trinket y racial por enemigo, **categorías de DR visibles junto a las barras de vida** | Es donde lees el DR del healer enemigo (núcleo de tu Fase 2) y el maná del healer rival (guerra de maná de Fase 1) | 🔴 Obligatorio |
| **MiniAuras** *(los documentos de julio lo llamaban "MiniCC" — nombre real verificado in-game 2026-09-11)* | Tracking de combate | Todo-en-uno que reemplaza a BigDebuffs + OmniBar + WeakAuras: CC en grande sobre frames y nameplates, CDs enemigos (kicks, ofensivos), **alerta "tu healer está en CC"**, alerta de CDs ofensivos enemigos, indicador de kicks jukeados (precognition) | El tracking de kicks enemigos decide cuándo es seguro hardcastear Cyclone; el indicador de precognition te marca la ventana dorada tras un fake exitoso | 🔴 Obligatorio |
| **FrameSort** | Raid frames | Fija el orden de los frames de tu grupo: tu personaje siempre abajo, party1 y party2 siempre en la misma posición entre rondas | **Infraestructura de tus macros:** sin él, dispel/Ironbark @party1/@party2 apuntan a la persona equivocada cuando el orden cambia entre rondas de Shuffle | 🔴 Obligatorio |
| **BetterBlizzPlates** | Nameplates | Mejora los nameplates nativos: CC a la derecha, DoTs arriba, borde blanco en tu target, **números 1/2/3 sobre cada enemigo**, **contador de combo points bajo tu target**, íconos sobre aliados | Los números 1/2/3 te dicen a quién le pega cada macro Cyclone @arena; el contador de combos es tu medidor de Maim (Fase 2) | 🔴 Obligatorio |
| **BetterBlizzFrames** | Unit frames | Limpia los frames nativos y añade indicadores de combate: avisa **cuándo un healer puede beber** (sale de combate) y cuándo un Rogue puede sapearte | Inteligencia para tu guerra de maná: ves las ventanas de bebida del healer enemigo (y las tuyas con Shadowmeld) | 🔴 Obligatorio |
| **Details!** | Medidor | Daño y sanación desglosados por partida, sobrevivió al Addon Apocalypse (el medidor nativo de Blizzard no guarda datos al desloguear) | Tus revisiones post-sesión: comparar tu sanación vs el healer rival, ver qué mató a tu aliado | 🟡 Recomendado |
| **BattleGroundEnemies Fixed** | RBG/BG | El "sArena de los battlegrounds": frames de todos los enemigos del BG con specs, targeteo desde el frame en cualquier punto del mapa | Tu herramienta cuando retomes RBG en Season 2 (tu bracket fuerte, 2100) | 🟡 Activar en S2 |
| **Battleground Win Conditions** | RBG/BG | Muestra las condiciones de victoria y objetivos del BG actual | Para tu rol de healer de FC: saber exactamente qué gana el mapa | 🟡 Activar en S2 |
| **Capping Battleground Timers** | RBG/BG | Timers de objetivos de BG (capturas, respawns, refuerzos) | Timing de rotaciones entre bases/objetivos en RBG | 🟡 Activar en S2 |
| **OmniBar** | Tracking (alternativa) | Barra dedicada de CDs enemigos (kicks, stuns, defensivos), lee el combat log (legal en Midnight) | Solo si el formato de MiniAuras no te convence para kicks — es redundante tenerlo junto a MiniAuras | ⚪ Opcional |
| **Diminish** | Tracking (alternativa) | Tracking dedicado de Diminishing Returns por categoría | Redundante con el DR nativo + sArena; considéralo solo si en Fase 2 quieres más detalle | ⚪ Opcional |
| **TalentLoadoutsEx** | Utilidad | Cambio rápido de loadouts de talentos entre partidas/rondas | Útil en Fase 4 (swaps por matchup). Su perfil de Skill Capped es premium, pero el addon en sí es gratis en CurseForge | ⚪ Fase 4 |
| **ArcUI** | Estética (premium SC) | Skin de interfaz exclusivo de suscriptores Skill Capped | No lo necesitas — cero impacto en rendimiento de juego | ⛔ No necesario |
| ~~WeakAuras~~ | — | Muerto en retail: sus devs no lo portarán a Midnight | Que ninguna guía vieja te lo haga instalar | ⛔ No instalar |
| ~~OmniCC~~ | — | Números de cooldown — ahora nativos en la UI base | Actívalo en Opciones, no con addon | ⛔ No instalar |
| ~~Gladius~~ | — | Frames de arena de la era anterior; sigue vivo pero desplazado por sArena Reloaded como estándar en retail | Redundante con sArena | ⛔ No instalar |

## Reglas simplificadas

1. **Una sola instalación:** CurseForge App → Skill Capped UI → marcar los 6 perfiles core (sArena, MiniAuras, FrameSort, BBP, BBF, Details) → Install → `/reload`.
2. **Los 🔴 son tu UI de arena; los 🟡 de BG se activan cuando vuelvas a RBG en S2.**
3. **Nada de la columna ⛔** — son reliquias de guías pre-Midnight.
4. **Verificación obligatoria en skirmish:** DR visible en frames, números 1/2/3 sobre enemigos, tu personaje abajo en raid frames, macros @party y @arena apuntando bien.
5. **Tras cada parche:** CurseForge → Update All → skirmish de verificación antes de puntuado.
