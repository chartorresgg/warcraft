# Addons, UI y Programas — PvP en Midnight (12.1)

> Verificado: 2026-07-12 · Revisado 2026-09-11 para S2: **el stack no cambió con 12.1.** Tras el parche, el protocolo es CurseForge → Update All → skirmish de verificación (ver `01-plan/guia_revalidacion_s2.md`).
> Fuentes: Skill Capped UI Guide (feb 2026), Icy Veins Best PvP Addons (may 2026), WowCarry PvP UI Guide (abr 2026), comunicados oficiales de Blizzard sobre la API, declaraciones del equipo de WeakAuras.
> ⚠️ Este archivo REEMPLAZA la lista de addons de la Fase 0.2 del roadmap original (OmniBar/Gladius/BigDebuffs/WeakAuras/OmniCC), que quedó obsoleta por el "Addon Apocalypse" de Midnight.



## 1. Qué pasó en Midnight (contexto en 60 segundos)

Blizzard introdujo los **"Secret Values"** en 12.0: los addons ya no pueden leer el estado de combate en tiempo real — solo pueden cambiar CÓMO se muestra la información que la UI base ya expone. Consecuencias:

- **WeakAuras está muerto en retail** — sus desarrolladores anunciaron oficialmente que no habrá versión para Midnight (siguen solo en Classic). Cualquier guía que te pida instalar WeakAuras está desactualizada.
- **Los helpers de rotación (Hekili etc.) fueron eliminados** — reemplazados por "Assisted Highlights" nativo.
- A cambio, **Blizzard integró en la UI base** gran parte de lo que antes daban los addons: Cooldown Manager, medidor de daño nativo, lectura de Diminishing Returns en los frames de arena, display de defensivos externos, números de cooldown en las barras (adiós OmniCC) y un Edit Mode potente.
- Los addons de PvP **sobrevivieron mejor que los de PvE** porque leen el combat log (legal) en vez de datos protegidos. Pero el stack estándar cambió de nombres.

**La filosofía nueva: configurar primero la UI base, y los addons solo rellenan huecos.**

## 2. PASO 1 — Configurar la UI base de Blizzard (antes de instalar nada)

> 🇪🇸 **Tu cliente está en español.** Los nombres de menú van en español, con el inglés entre paréntesis (las guías y vídeos que consultes estarán en inglés).
>
> **Las dos teclas que abren todo:** `ESC → Opciones` (Options) para los ajustes, y `ESC → Editar` / **Modo de edición** (Edit Mode) para mover y activar elementos de la interfaz.
>
> ⚠️ Las rutas exactas de submenú pueden variar con los parches. Si no encuentras una opción donde dice la tabla, **usa el buscador de la ventana de Opciones** (arriba a la derecha): escribe una palabra clave en español y te lleva directo.


| Ajuste (ES / EN)                                                                             | Dónde                                     | Por qué te importa                                                                                                                                |
| -------------------------------------------------------------------------------------------- | ----------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Gestor de tiempos de reutilización** (Cooldown Manager)                                    | Modo de edición (Edit Mode)               | Tracker nativo de tus CDs ofensivos/defensivos/utilidad. Wowhead tiene strings de importación por clase ("starter UI pack") — importa el de Druid |
| **Números de tiempo de reutilización en las barras** (cooldown numbers)                      | Opciones → Barras de acción (Action Bars) | Reemplaza a OmniCC. Actívalo y no instales nada para esto                                                                                         |
| **Barras de lanzamiento en placas de nombre enemigas** (cast bars on nameplates)             | Opciones → Placas de nombre (Nameplates)  | La mejora de legibilidad #1 según las guías: ves cada cast enemigo sobre su cabeza                                                                |
| **Placas de nombre siempre visibles + apilado vertical** (always show nameplates / stacking) | Opciones → Placas de nombre (Nameplates)  | Con solo TUS debuffs mostrados (lo demás lo pone MiniCC)                                                                                          |
| **Retratos como íconos de clase** (class icon portraits)                                     | Opciones → Interfaz (Interface)           | Lees la comp enemiga de un vistazo                                                                                                                |
| **Marcos de banda: barra de poder + colores de clase + mostrar mascotas** (raid frames)      | Opciones → Marcos de banda (Raid Frames)  | Ves el maná del healer aliado y distingues clases al instante                                                                                     |
| **Lectura de DR en los marcos de arena** (diminishing returns)                               | Nativa desde 12.0                         | El juego ya muestra diminishing returns en los frames — antes esto requería addon                                                                 |
| **Visualización de defensivos externos** (external defensives display)                       | Modo de edición (Edit Mode)               | Ves los externos activos (tu Ironbark / Corteza de hierro incluido) de forma nativa                                                               |
| **Pantalla de recursos personales** (Personal Resource Display)                              | Opciones → Interfaz (Interface)           | Tus recursos bajo tu personaje: no apartas la vista del centrqso de la pantalla                                                                   |
| **Objetivo del objetivo** (Target of Target)                                                 | Opciones → Interfaz (Interface)           | Ves a quién está pegando tu objetivo — quién va a morir antes                                                                                     |


> 💡 **Atajo que te ahorra todo esto:** el addon **Skill Capped UI** (§7) configura la mayoría de estos ajustes automáticamente, incluidos CVars ocultos que no están en ningún menú (como el *Spell Queue Window* ajustado a tu latencia). Si lo instalas, revisa esta tabla solo para lo que quieras afinar a mano.



## 3. PASO 2 — El stack de addons PvP de Midnight (el nuevo estándar)


| Addon                                       | Reemplaza a                                    | Qué hace                                                                                                                                                                                                              | Prioridad                                  |
| ------------------------------------------- | ---------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------ |
| **sArena Reloaded**                         | Gladius                                        | El nuevo estándar de frames de arena: frames espejados, barras con color de clase, cast bars grandes, trinket y racial por enemigo, categorías de DR junto a las barras de vida                                       | 🔴 Obligatorio                             |
| **MiniCC**                                  | BigDebuffs + OmniBar + WeakAuras (todo en uno) | CC gigante en frames y nameplates, tracking de CDs enemigos (kicks, ofensivos), **alerta de "tu healer está en CC"**, alerta de CDs ofensivos enemigos, indicador de precognition (kicks jukeados)                    | 🔴 Obligatorio                             |
| **FrameSort**                               | — (nuevo imprescindible)                       | **Fija el orden de tus raid frames: party1 y party2 SIEMPRE en la misma posición entre rondas.** Sin esto, tus macros @party1/@party2 le pegan a la persona equivocada cuando el orden cambia entre rondas de Shuffle | 🔴 Obligatorio — tus macros dependen de él |
| **OmniBar**                                 | — (sobrevivió)                                 | Barra de CDs enemigos clásica. Redundante si MiniCC te basta; algunos prefieren su formato de barra separada para kicks                                                                                               | 🟡 Opcional                                |
| **BetterBlizzPlates** (+ BetterBlizzFrames) | Plater parcialmente                            | Retoque fino de los nameplates nativos: tamaño, color, orden, IDs de arena en vez de nombres                                                                                                                          | 🟡 Opcional                                |
| **Diminish**                                | —                                              | Tracking de DR dedicado. Redundante con el DR nativo + sArena para empezar; útil si quieres más detalle en Fase 2                                                                                                     | 🟡 Opcional                                |
| **TalentLoadoutsEx**                        | —                                              | Cambio rápido de loadouts de talentos entre rondas/partidas — útil cuando llegues a los swaps de matchup (Fase 4)                                                                                                     | 🟡 Opcional                                |
| **Gladius**                                 | —                                              | Sigue vivo y actualizado para 12.0, pero las guías actuales coinciden: sArena Reloaded lo desplazó como estándar en retail                                                                                            | ⚪ Alternativa                              |
| ~~WeakAuras~~                               | —                                              | Muerto en retail. No instalar                                                                                                                                                                                         | ⛔                                          |
| ~~OmniCC~~                                  | —                                              | Innecesario: números de CD nativos                                                                                                                                                                                    | ⛔                                          |


**Atajo recomendado — Skill Capped UI (addon):** Skill Capped publicó un addon que instala y **auto-configura los perfiles de todo el stack anterior en un clic** (sArena Reloaded con DR visible, MiniCC completo, FrameSort con tu personaje abajo, Edit Mode centrado, más ajustes ocultos). Dado que ya usas Skill Capped como fuente, es la ruta de menor fricción: resultado profesional en 10 minutos en vez de una tarde de configuración manual. Búscalo como "Skill Capped UI" en su web/CurseForge. Si prefieres control total, configura manualmente con las tablas de arriba.

## 4. PASO 3 — Programas de escritorio


| Programa                          | ¿Lo necesitas?            | Para qué                                                                                                                                                                                       |
| --------------------------------- | ------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **CurseForge App**                | ✅ Sí — el primero         | El gestor de addons estándar: instala y actualiza todo el stack con un clic. Instálalo en modo standalone (durante la instalación puedes desmarcar/omitir la capa de Overwolf si te la ofrece) |
| **OBS Studio**                    | ✅ Sí — desde Fase 2       | Gratuito, para grabar tus VODs con "replay buffer". Es LA herramienta de tu Fase 4 (revisión de partidas). Instálalo ya, configúralo cuando lleguemos ahí                                      |
| **Discord**                       | ✅ Ya lo tienes            | Tu transición a equipos coordinados vive aquí                                                                                                                                                  |
| **Check-PvP** (check-pvp.fr, web) | ✅ Guárdalo en favoritos   | Perfil PvP de cualquier jugador: experiencia real, ratings históricos, alts. Tu herramienta de Fase 3 para evaluar compañeros de LFG antes de invertir tardes con ellos                        |
| **Murlok.io** (web)               | ✅ Ya lo usas              | Datos vivos de builds top. Tu referencia permanente                                                                                                                                            |
| **WoWUp**                         | ⚪ Alternativa             | Gestor de addons alternativo a CurseForge, más ligero y open source. Uno u otro, no ambos                                                                                                      |
| **WarcraftLogs**                  | ❌ No para ti              | Análisis de logs de RAID/M+. Ecosistema PvE — un jugador 100% PvP no le saca valor                                                                                                             |
| **Archon App**                    | ❌ No para ti              | Builds y análisis orientados a M+/raid (del ecosistema WarcraftLogs). Murlok cubre tu caso PvP                                                                                                 |
| **Overwolf**                      | ❌ Evítalo como plataforma | Es la plataforma-contenedor con overlays y anuncios. No aporta nada que necesites; consume FPS (y tú andas en 58 en team fights)                                                               |




## 5. Orden de instalación (una sesión de ~1 hora)

1. Instalar **CurseForge App** → con él instalar **sArena Reloaded, MiniCC, FrameSort** (o el addon **Skill Capped UI** que configura todo).
2. Configurar la **UI base** con la tabla del Paso 1 (15 min). Importar el Gestor de tiempos de reutilización (Cooldown Manager) de Druid desde el starter pack de Wowhead.
3. Entrar a un **combate de prueba / skirmish** y verificar que ves: (a) DR en los marcos de arena, (b) CC gigante en los marcos, (c) tu orden de grupo fijo, (d) barras de lanzamiento enemigas en las placas de nombre (nameplates).
4. Probar las macros @party1/@party2 con FrameSort activo: confirmar que party1 es SIEMPRE el marco de arriba.
5. Instalar **OBS** (sin configurar aún) y guardar **Check-PvP** en favoritos.
6. Actualizar `macros_y_ui.md` con el stack final.



## 6. Reglas simplificadas

1. **UI base primero, addons después.** Blizzard ya te da DR, cooldown numbers, cast bars y defensivos externos gratis.
2. **El stack 2026 son 3 addons:** sArena Reloaded + MiniCC + FrameSort. Todo lo demás es opcional.
3. **FrameSort no es cosmético: es infraestructura de tus macros.** Sin orden fijo de party, @party1/@party2 son ruleta rusa en Shuffle.
4. **WeakAuras murió — que ninguna guía vieja te lo haga instalar.** Lo mismo OmniCC y los rotation helpers.
5. **Un solo gestor de addons** (CurseForge App) y **un solo programa extra** por ahora (OBS). Overwolf, WarcraftLogs y Archon no aportan a un jugador 100% PvP.
6. **Menos es más con 58 FPS:** cada addon y overlay cuesta rendimiento. El stack mínimo también es el más rápido.
7. **Tras cada parche** (12.1 en agosto): abrir CurseForge, actualizar todo, y entrar a un skirmish de verificación antes de colar puntuado.

---



## 7. Skill Capped UI — instalación y configuración (guía oficial, feb 2026)



### Qué incluye (y qué cuesta)


| Perfil                                                   | ¿Gratis?                 | Qué te da su perfil pre-configurado                                                                                                                                                                                                 |
| -------------------------------------------------------- | ------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **sArena Reloaded**                                      | ✅                        | Categorías de DR a la IZQUIERDA de las barras de vida, cast bar con más margen (casts visibles de un vistazo), íconos de dispel y racial reubicados sin solaparse                                                                   |
| **MiniCC**                                               | ✅                        | Todo configurado: CC claro, tracking de CDs, alerta de CDs ofensivos enemigos y **notificación de "tu healer está en CC"**                                                                                                          |
| **FrameSort**                                            | ✅                        | Tu personaje SIEMPRE abajo en los raid frames → party1/party2 fijos → tus macros nunca fallan                                                                                                                                       |
| **BetterBlizzPlates**                                    | ✅                        | CC a la derecha de los nameplates enemigos, DoTs arriba, borde blanco en tu target, **números 1/2/3 sobre cada enemigo** (sabes a quién le pega cada macro @arena), **contador de combo points bajo tu target** (tu Maim de Fase 2) |
| **BetterBlizzFrames**                                    | ✅                        | Menos clutter + indicador de combate que avisa **cuándo el healer enemigo puede beber** (¡y cuándo puedes tú!) y cuándo un Rogue puede sapearte                                                                                     |
| **Details**                                              | ✅                        | Medidor de daño/sanación para tus revisiones post-partida                                                                                                                                                                           |
| **BattleGroundEnemies Fixed + Win Conditions + Capping** | ✅                        | El "sArena de los BGs" — actívalos cuando retomes RBG en S2                                                                                                                                                                         |
| ArcUI, Talent Loadout Ex                                 | 💰 Premium (suscripción) | Extras de estética y gestión de loadouts. **NO los necesitas** — el valor real está en los perfiles gratuitos                                                                                                                       |




### Ajustes ocultos (CVars) que configura solo — los que te importan


| Ajuste                                                                          | Por qué te importa a TI                                                                                                                                              |
| ------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Spell Queue Window = tu latencia + 100**                                      | Con tus ~200 ms quedará en ~300: tus hechizos se encadenan sin micro-huecos entre GCDs. Es EL ajuste que los jugadores con ping alto deben tener y casi nadie conoce |
| Cámara al máximo + sin auto-ajuste                                              | Más campo visual = mejor lectura de posicionamiento (tu debilidad declarada)                                                                                         |
| Sticky targeting                                                                | Un misclick al suelo ya no te des-targetea                                                                                                                           |
| Texturas proyectadas reducidas                                                  | Ves el Ring of Frost y AoEs enemigos con claridad                                                                                                                    |
| Mascotas en raid frames, sin texto de combate en retrato, sin errores de script | Limpieza general                                                                                                                                                     |




### Pasos de instalación

1. **CurseForge App → buscar "Skill Capped UI" → Install** (o desde skill-capped.com/wow/addons). Instalará también los addons del stack si te faltan.
2. Entrar al juego → aparece la **pantalla de bienvenida del addon**.
3. El campo de Battle.net tag / código premium es **solo para suscriptores** — sáltalo o déjalo vacío: los perfiles core son gratis.
4. En la pantalla de selección: **marcar los 6 perfiles core** (sArena, MiniCC, FrameSort, BBP, BBF, Details). Los de BG puedes marcarlos ya o esperar a S2. → **Install**.
5. `/reload` y revisar el **Edit Mode**: el perfil centra raid frames y focus frame a la misma distancia periférica de los frames de arena — si algo te estorba, se arrastra desde ahí sin romper nada.



### Verificación (skirmish de 5 min — no saltar)

- ☐ Marcos de arena con DR visible a la izquierda de las barras
- ☐ Números 1/2/3 sobre las placas de nombre (nameplates) enemigas → probar Cyclone (Ciclón) @arena1 contra el correcto
- ☐ Tu personaje abajo en los marcos de banda (raid frames) → probar dispel @party1 y @party2
- ☐ Alerta de MiniCC visible (que un enemigo te CCee y mira la notificación)
- ☐ Barras de lanzamiento (cast bars) enemigas legibles a un vistazo
- ☐ FPS estables (si bajan de tus 58 habituales, desactivar Details primero)
- ☐ **Las 11 macros sin ícono "?"** — si alguna lo tiene, el nombre del hechizo está mal escrito (ver `macros_resto_druid.md`)

Soporte oficial: canal de addons en el Discord de Skill Capped (discord.gg/scwow).

### Dos advertencias

1. **El perfil pisa tu configuración previa de esos addons.** Para ti es irrelevante (partes de cero) — pero anótalo para el futuro: reinstalar el perfil = perder ajustes manuales.
2. **Tu scroll abajo y tus keybinds NO se tocan** — el addon configura interfaz, no teclas. Tu mapa de binds del archivo de macros sigue siendo tarea tuya.

