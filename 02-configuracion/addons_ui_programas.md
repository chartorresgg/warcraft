# Addons, UI y Programas — PvP en Midnight (12.0.7)

> Verificado: 2026-07-12. Fuentes: Skill Capped UI Guide (feb 2026), Icy Veins Best PvP Addons (may 2026), WowCarry PvP UI Guide (abr 2026), comunicados oficiales de Blizzard sobre la API, declaraciones del equipo de WeakAuras.
> ℹ️ Este archivo es la referencia detallada de la Fase 0.2 del roadmap (sincronizado 2026-07-12). La lista original (OmniBar/Gladius/BigDebuffs/WeakAuras/OmniCC) quedó obsoleta por el "Addon Apocalypse" de Midnight.

## 1. Qué pasó en Midnight (contexto en 60 segundos)

Blizzard introdujo los **"Secret Values"** en 12.0: los addons ya no pueden leer el estado de combate en tiempo real — solo pueden cambiar CÓMO se muestra la información que la UI base ya expone. Consecuencias:

- **WeakAuras está muerto en retail** — sus desarrolladores anunciaron oficialmente que no habrá versión para Midnight (siguen solo en Classic). Cualquier guía que te pida instalar WeakAuras está desactualizada.
- **Los helpers de rotación (Hekili etc.) fueron eliminados** — reemplazados por "Assisted Highlights" nativo.
- A cambio, **Blizzard integró en la UI base** gran parte de lo que antes daban los addons: Cooldown Manager, medidor de daño nativo, lectura de Diminishing Returns en los frames de arena, display de defensivos externos, números de cooldown en las barras (adiós OmniCC) y un Edit Mode potente.
- Los addons de PvP **sobrevivieron mejor que los de PvE** porque leen el combat log (legal) en vez de datos protegidos. Pero el stack estándar cambió de nombres.

**La filosofía nueva: configurar primero la UI base, y los addons solo rellenan huecos.**

## 2. PASO 1 — Configurar la UI base de Blizzard (antes de instalar nada)

| Ajuste | Dónde | Por qué te importa |
|---|---|---|
| **Cooldown Manager** | Edit Mode (Modo de edición) | Tracker nativo de tus CDs ofensivos/defensivos/utilidad. Wowhead tiene strings de importación por clase ("starter UI pack") — importa el de Druid |
| **Números de cooldown en barras** | Opciones → Combate/Barras de acción | Reemplaza a OmniCC. Actívalo y no instales nada para esto |
| **Cast bars en nameplates enemigos** | Opciones → Nameplates | La mejora de legibilidad #1 según las guías: ves cada cast enemigo sobre su cabeza |
| **Nameplates siempre visibles + apilado vertical** | Opciones → Nameplates | Con solo TUS debuffs mostrados (lo demás lo pone MiniCC) |
| **Retratos como íconos de clase** | Opciones → Interfaz | Lees la comp enemiga de un vistazo |
| **Raid frames: barra de poder + colores de clase + mostrar mascotas** | Opciones → Raid frames | Ves el maná del healer aliado y distingues clases al instante |
| **Lectura de DR en frames de arena** | Nativa desde 12.0 | El juego ya muestra diminishing returns en los frames — antes esto requería addon |
| **Display de defensivos externos** | Edit Mode | Ves los externos activos (tu Ironbark incluido) de forma nativa |
| **Personal Resource Display + Target of Target** | Opciones | Recursos propios bajo tu personaje y quién golpea a quién |

## 3. PASO 2 — El stack de addons PvP de Midnight (el nuevo estándar)

| Addon | Reemplaza a | Qué hace | Prioridad |
|---|---|---|---|
| **sArena Reloaded** | Gladius | El nuevo estándar de frames de arena: frames espejados, barras con color de clase, cast bars grandes, trinket y racial por enemigo, categorías de DR junto a las barras de vida | 🔴 Obligatorio |
| **MiniCC** | BigDebuffs + OmniBar + WeakAuras (todo en uno) | CC gigante en frames y nameplates, tracking de CDs enemigos (kicks, ofensivos), **alerta de "tu healer está en CC"**, alerta de CDs ofensivos enemigos, indicador de precognition (kicks jukeados) | 🔴 Obligatorio |
| **FrameSort** | — (nuevo imprescindible) | **Fija el orden de tus raid frames: party1 y party2 SIEMPRE en la misma posición entre rondas.** Sin esto, tus macros @party1/@party2 le pegan a la persona equivocada cuando el orden cambia entre rondas de Shuffle | 🔴 Obligatorio — tus macros dependen de él |
| **OmniBar** | — (sobrevivió) | Barra de CDs enemigos clásica. Redundante si MiniCC te basta; algunos prefieren su formato de barra separada para kicks | 🟡 Opcional |
| **BetterBlizzPlates** (+ BetterBlizzFrames) | Plater parcialmente | Retoque fino de los nameplates nativos: tamaño, color, orden, IDs de arena en vez de nombres | 🟡 Opcional |
| **Diminish** | — | Tracking de DR dedicado. Redundante con el DR nativo + sArena para empezar; útil si quieres más detalle en Fase 2 | 🟡 Opcional |
| **TalentLoadoutsEx** | — | Cambio rápido de loadouts de talentos entre rondas/partidas — útil cuando llegues a los swaps de matchup (Fase 4) | 🟡 Opcional |
| **Gladius** | — | Sigue vivo y actualizado para 12.0, pero las guías actuales coinciden: sArena Reloaded lo desplazó como estándar en retail | ⚪ Alternativa |
| ~~WeakAuras~~ | — | Muerto en retail. No instalar | ⛔ |
| ~~OmniCC~~ | — | Innecesario: números de CD nativos | ⛔ |

**Atajo recomendado — Skill Capped UI (addon):** Skill Capped publicó un addon que instala y **auto-configura los perfiles de todo el stack anterior en un clic** (sArena Reloaded con DR visible, MiniCC completo, FrameSort con tu personaje abajo, Edit Mode centrado, más ajustes ocultos). Dado que ya usas Skill Capped como fuente, es la ruta de menor fricción: resultado profesional en 10 minutos en vez de una tarde de configuración manual. Búscalo como "Skill Capped UI" en su web/CurseForge. Si prefieres control total, configura manualmente con las tablas de arriba.

## 4. PASO 3 — Programas de escritorio

| Programa | ¿Lo necesitas? | Para qué |
|---|---|---|
| **CurseForge App** | ✅ Sí — el primero | El gestor de addons estándar: instala y actualiza todo el stack con un clic. Instálalo en modo standalone (durante la instalación puedes desmarcar/omitir la capa de Overwolf si te la ofrece) |
| **OBS Studio** | ✅ Sí — desde Fase 2 | Gratuito, para grabar tus VODs con "replay buffer". Es LA herramienta de tu Fase 4 (revisión de partidas). Instálalo ya, configúralo cuando lleguemos ahí |
| **Discord** | ✅ Ya lo tienes | Tu transición a equipos coordinados vive aquí |
| **Check-PvP** (check-pvp.fr, web) | ✅ Guárdalo en favoritos | Perfil PvP de cualquier jugador: experiencia real, ratings históricos, alts. Tu herramienta de Fase 3 para evaluar compañeros de LFG antes de invertir tardes con ellos |
| **Murlok.io** (web) | ✅ Ya lo usas | Datos vivos de builds top. Tu referencia permanente |
| **WoWUp** | ⚪ Alternativa | Gestor de addons alternativo a CurseForge, más ligero y open source. Uno u otro, no ambos |
| **WarcraftLogs** | ❌ No para ti | Análisis de logs de RAID/M+. Ecosistema PvE — un jugador 100% PvP no le saca valor |
| **Archon App** | ❌ No para ti | Builds y análisis orientados a M+/raid (del ecosistema WarcraftLogs). Murlok cubre tu caso PvP |
| **Overwolf** | ❌ Evítalo como plataforma | Es la plataforma-contenedor con overlays y anuncios. No aporta nada que necesites; consume FPS (y tú andas en 58 en team fights) |

## 5. Orden de instalación (una sesión de ~1 hora)

1. Instalar **CurseForge App** → con él instalar **sArena Reloaded, MiniCC, FrameSort** (o el addon **Skill Capped UI** que configura todo).
2. Configurar la **UI base** con la tabla del Paso 1 (15 min). Importar el Cooldown Manager de Druid desde el starter pack de Wowhead.
3. Entrar a un **skirmish** de prueba: verificar que ves (a) DR en frames de arena, (b) CC gigante en frames, (c) tu orden de party fijo, (d) cast bars enemigas en nameplates.
4. Probar las macros @party1/@party2 con FrameSort activo: confirmar que party1 es SIEMPRE el frame de arriba.
5. Instalar **OBS** (sin configurar aún) y guardar **Check-PvP** en favoritos.
6. Actualizar `02-configuracion/macros_y_ui.md` con el stack final.

## 6. Reglas simplificadas

1. **UI base primero, addons después.** Blizzard ya te da DR, cooldown numbers, cast bars y defensivos externos gratis.
2. **El stack 2026 son 3 addons:** sArena Reloaded + MiniCC + FrameSort. Todo lo demás es opcional.
3. **FrameSort no es cosmético: es infraestructura de tus macros.** Sin orden fijo de party, @party1/@party2 son ruleta rusa en Shuffle.
4. **WeakAuras murió — que ninguna guía vieja te lo haga instalar.** Lo mismo OmniCC y los rotation helpers.
5. **Un solo gestor de addons** (CurseForge App) y **un solo programa extra** por ahora (OBS). Overwolf, WarcraftLogs y Archon no aportan a un jugador 100% PvP.
6. **Menos es más con 58 FPS:** cada addon y overlay cuesta rendimiento. El stack mínimo también es el más rápido.
7. **Tras cada parche** (12.1 en agosto): abrir CurseForge, actualizar todo, y entrar a un skirmish de verificación antes de colar puntuado.
