# Fuentes del Proyecto

> Todas las fuentes consultadas para construir este sistema de entrenamiento, con qué se sacó de cada una y cuándo caduca.
> Última actualización: 2026-09-12.

---

## 1. Cómo leer esta lista

| Tipo | Caduca | Ejemplos |
|---|---|---|
| 🔴 **Datos de meta** | **Con cada parche** | Builds, talentos, stats, gemas, comps, win rates |
| 🟡 **Mecánicas del juego** | Con reworks grandes | Sistema de DR, funcionamiento de hechizos, categorías de CC |
| 🟢 **Consejo situacional** | **No caduca** | Regla de trinket, árbol de decisión de Cyclone, protocolo de comunicación, gestión mental |

**Regla de precedencia del proyecto:** el **tooltip in-game gana** sobre cualquier fuente de esta lista. Midnight rediseñó parte del kit y las traducciones al español a veces no coinciden con las guías.

---

## 2. Fuentes primarias — datos vivos 🔴

### Murlok.io — la fuente más usada del proyecto

Datos en tiempo real de los **top 50 jugadores** de cada bracket (US, EU, KR, TW), refrescados cada 8 horas vía la API de Blizzard. Es la referencia para todo lo que sea "qué juegan los mejores".

| Página | Qué se sacó |
|---|---|
| [3v3](https://murlok.io/druid/restoration/3v3) | Hero talent (Keeper 42/50), tríada de PvP talents, stats de arena, gemas, enchants, embellishments, trinkets, raza |
| [Solo Shuffle](https://murlok.io/druid/restoration/solo) | Build del bracket principal del jugador |
| [Battleground Blitz](https://murlok.io/druid/restoration/blitz) | Build de Blitz: stats invertidos, los 3 talentos casi unánimes del formato |
| [RBG](https://murlok.io/druid/restoration/rbg) | Build de RBG de grupo |
| [Talentos](https://murlok.io/druid/restoration/talents) | Heatmap general del spec |

> **Cómo usarla:** el heatmap muestra cuántos de los top 50 usan cada talento. 48-50 = core, 15-45 = flexible por matchup, <10 = ignóralo aunque una guía lo recomiende.

### Blizzard — fuente oficial 🔴

| Fuente | Qué se sacó |
|---|---|
| [Hotfixes del 1 de septiembre de 2026](https://news.blizzard.com/en-us/article/24296142/hotfixes-september-1-2026) | **Los nerfs que ninguna guía tenía todavía**: Swiftmend −20% en PvP, Regrowth −20%, sanación general −5%, Incarnation acortado, Innervate al 20% (no 25%) |
| Notas de parche y de desarrollo | Cambios de clase, sistema de DR |

> **Lección aprendida:** los hotfixes de las 2-3 semanas posteriores a un parche importan tanto como el parche. El PTR acierta en la dirección y falla en los números.

---

## 3. Guías editoriales 🟡

### Icy Veins

Guía de Mysticall (múltiple Rank 1). Editorial, no estadística — a veces recomienda cosas que el ladder no juega.

| Página | Qué se sacó |
|---|---|
| [Resto Druid PvP Guide 12.1](https://www.icy-veins.com/wow/restoration-druid-pvp-guide) | Los 4 usos de Cyclone, regla del trinket enemigo, cadenas de CC |
| [PvP Talents and Builds](https://www.icy-veins.com/wow/restoration-druid-pvp-talents-and-builds) | PvP talents situacionales (Thorns, High Winds, Disentanglement) |
| [Best Arena Compositions](https://www.icy-veins.com/wow/restoration-druid-pvp-best-arena-compositions) | Comps de 3v3 y su lógica |
| [Stat Priority, Gear and Trinkets](https://www.icy-veins.com/wow/restoration-druid-pvp-stat-priority-gear-and-trinkets) | Contraste con los datos de Murlok |
| [Notas de desarrollo 12.1 — DR](https://www.icy-veins.com/wow/news/class-changes-diminishing-returns-midnight-12-1-ptr-development-notes-june-30th/) | Confirmación del DR 16→20 seg |
| [Battleground Blitz Guide](https://www.icy-veins.com/wow/battleground-blitz-guide) | Mecánicas del formato |

> ⚠️ **Dos advertencias sobre Icy Veins en este proyecto:**
> 1. Recomienda **Ancient of Lore**, que el ladder juega 3/50. Cuando la recomendación editorial choca con el dato vivo, **gana el dato**.
> 2. Sus descripciones de comps mencionan **Mighty Bash**, que Resto **no tiene** en Midnight. Son textos heredados de expansiones anteriores.

### Skill Capped

| Página | Qué se sacó |
|---|---|
| [Talents & Builds S2](https://www.skill-capped.com/wowarticles/guides/restoration-druid-pvp-guide/talents/) | Build estándar, import strings |
| [Cambios de 12.1](https://www.skill-capped.com/wowarticles/guides/restoration-druid-pvp-guide/midnight-changes/) | Overgrowth, Flash of Clarity, Genesis, Abundance rediseñado |
| [Gearing](https://www.skill-capped.com/wowarticles/guides/restoration-druid-pvp-guide/gearing/) | Gemas, embellishments |
| [Best Comps](https://www.skill-capped.com/wowarticles/guides/restoration-druid-pvp-guide/best-comps/) | Comps de S2 con win rates |
| Skill Capped UI (addon) | El stack completo de addons y los CVars ocultos (Spell Queue Window) |

### Method

| Página | Qué se sacó |
|---|---|
| [Resto Druid — Talents](https://www.method.gg/guides/restoration-druid/talents) | Qué habilidades son activas y cuáles pasivas; el talento **Lifetreading** |
| [Playstyle and Rotation](https://www.method.gg/guides/restoration-druid/playstyle-and-rotation) | Prioridad de casteo, mantenimiento de HoTs |

> ⚠️ Method es una fuente **de PvE**. Se usó solo para mecánica de hechizos (que no cambia entre modos), nunca para builds o prioridades — en PvE recomiendan Wildstalker, que en PvP es minoritario (8/50).

### Otras

| Fuente | Qué se sacó |
|---|---|
| [ArenaCoach — S1](https://arenacoach.gg/guides/restoration-druid-pvp-guide-midnight-season-1) | Win rates de comps y errores comunes (datos de S1) |
| [Method — Omnium Folio](https://www.method.gg/guides/best-omnium-folio-runes-builds-in-midnight-wow) | Runas del Folio |
| [ConquestCapped — Omnium Folio](https://conquestcapped.com/guides/wow/omnium-folio/) | Contraste de runas PvP vs PvE |
| Wowhead | Traducciones, IDs de hechizos, starter UI pack del Cooldown Manager |
| [WowChakra](https://www.wowchakra.com/wow/descripciones-de-las-facultades-y-talentos-de-druida-en-dragonflight) | **Traducciones EN→ES de los hechizos de druida** |

---

## 4. Herramientas 🟢

| Herramienta | Para qué | Enlace |
|---|---|---|
| **CurseForge App** | Gestor de addons | curseforge.com |
| **OBS Studio** | Grabación de VODs (Fase 4) | obsproject.com |
| **Check-PvP** | Historial PvP de cualquier jugador — evaluar compañeros antes de invertir tardes | [check-pvp.fr](https://check-pvp.fr) |
| **ArenaMaster** | LFG por bracket, rating y objetivo — buscar equipo (Fase 3) | [arenamaster.io/lfg](https://www.arenamaster.io/lfg) |
| **Discord** | Comunicación de equipo | — |

---

## 5. Lo que NO se usó, y por qué

| Fuente | Por qué se descartó |
|---|---|
| **WarcraftLogs** | Análisis de raid y M+. Ecosistema PvE: un jugador 100% PvP no le saca valor |
| **Archon App** | Builds orientadas a M+/raid |
| **Maxroll** (guías de M+) | Solo se consultó su explicación del sistema de DR, no sus builds |
| **Guías de expansiones anteriores** | Midnight rediseñó el kit. Cualquier guía que mencione Mighty Bash para Resto, o que pida instalar WeakAuras, está obsoleta |

---

## 6. Cuándo revalidar

Ejecuta `01-plan/guia_revalidacion_s2.md` cuando:

- Llegue un **parche mayor**
- Pasen **2-3 semanas tras un parche** (por los hotfixes)
- Empiece una **temporada nueva**

**Orden de consulta en una revalidación:**
1. Notas oficiales de Blizzard (qué cambió)
2. Hotfixes posteriores (qué se ajustó después)
3. Murlok.io (qué juegan los top **una semana después**, no el día 1)
4. Icy Veins / Skill Capped (cómo interpretarlo)

---

## 7. Reglas simplificadas

1. **El tooltip in-game gana sobre todo lo demás.**
2. **Dato vivo (Murlok) > recomendación editorial (Icy Veins)** cuando choquen.
3. **Los hotfixes importan tanto como el parche.** Revísalos siempre.
4. **Method y Maxroll son PvE:** útiles para mecánica de hechizos, nunca para builds.
5. **El heatmap de Murlok necesita ~1 semana tras un parche** para decir la verdad.
6. **Cualquier guía que mencione Mighty Bash para Resto o WeakAuras está obsoleta.**
