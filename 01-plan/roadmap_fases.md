# Roadmap de Entrenamiento — Resto Druid PvP (Midnight)

> Generado: 2026-07-11 | Parche verificado: **12.0.7, Midnight Season 1**
> Próximo hito del juego: **12.1 / Season 2 a mediados de agosto** (~5 semanas)
> Fuentes principales: Icy Veins PvP (Mysticall, multi-R1), Skill Capped, Murlok.io (datos live top 50), ArenaCoach (datos de ladder), notas de desarrollo 12.1 PTR.

---

## ⚠️ Decisión estratégica previa: Season 1 termina en ~5 semanas

Season 2 llega con 12.1 a mediados de agosto. Con 8 h/semana, **no vas a superar tu récord de 1750/2100 en lo que queda de S1** — y no deberías intentarlo. La jugada correcta:

- **Semanas 1-5 (resto de S1):** laboratorio. Fases 0, 1 y arranque de la 2. Cero presión por rating; el rating de S1 ya no importa.
- **Season 2 en adelante:** ahí empieza el push real, con fundamentos sólidos y (idealmente) compañeros ya identificados.

**Qué de este documento caduca con 12.1** (revisar en agosto):

- Builds de talentos y PvP talents → *Ancient of Lore* regresa como PvP talent, *Genesis* se rediseña, *Overgrowth* y *Flash of Clarity* son talentos nuevos, *Nature's Splendor* desaparece.
- Gestión de maná → **Innervate se rediseña**: pasa de "hechizos gratis 8 seg" a "regenera 25% del maná máximo en 8 seg". La guerra de maná cambia de reglas.
- Timing de cadenas de CC → el reset de DR sube de **16 a 20 segundos**. Las ventanas entre goes se alargan.
- Tuning general (Wild Growth +20% healing pero +15% maná, Lifebloom -20% maná, etc.).
- **Lo que NO caduca:** todo lo mecánico — posicionamiento, fake casting, lectura de DR, comunicación, hábitos. Ese es el 80% del roadmap.

---



## FASE 0 — Cimientos técnicos (Semanas 1-2, ~16 h)

**Objetivo:** dejar de jugar con desventaja de herramientas. Hoy juegas sin addons y sin macros: es como ir al gimnasio en sandalias. Antes de entrenar técnica, necesitas el equipo.

### 0.1 Build y gear (verificar contra fuentes vivas, no memorizar)

- **Talentos y PvP talents:** importar el build estándar de Skill Capped para S1 (build "Standard": *Early Spring*, *Call of Ohn'ahra*, *Forest Guardian*) y contrastar con el heatmap de Murlok.io 3v3 (datos de top 50, actualizado cada 8 h). PvP talents situacionales a tener aprendidos: *Thorns* (vs doble melee), *Disentanglement* (vs comps con slows), *High Winds* (Cyclone defensivo vs equipos sin kicks).
- **Hero Talent:** ya juegas *Keeper of the Grove*; valida en Murlok.io qué usan los top de 3v3 este parche antes de S2 (los dos árboles son viables, pero el dominante cambia con tuning).
- **Stats:** Mastery > Versatility > Haste > Crit (datos de ladder). Gemas y encantamientos: copiar los más usados en Murlok.io 3v3 — no teorices, son datos vivos.
- **Omnium Folio (nuevo en 12.0.7):** completar la cadena de misiones y elegir las runas PvP recomendadas en la página de builds de Icy Veins.
- **iLvl:** a 298 estás bien para practicar; capea el gear PvP semanal para llegar a S2 con base.



### 0.2 UI base + addons (instalación mínima viable — una sesión de ~1 hora)

> ⚠️ Actualizado 2026-07-12: la lista original (Gladius/OmniBar/BigDebuffs/OmniCC/WeakAuras) quedó obsoleta por el "Addon Apocalypse" de Midnight — WeakAuras está muerto en retail y OmniCC es innecesario. El detalle completo, la configuración de la UI base y el orden de instalación están en `02-configuracion/addons_ui_programas.md`.

**Primero la UI base de Blizzard** (Cooldown Manager, números de CD nativos, cast bars en nameplates, DR nativo en frames de arena), **después el stack de 3 addons:**


| Addon                | Para qué                                                                                                                 |
| -------------------- | ------------------------------------------------------------------------------------------------------------------------ |
| **sArena Reloaded**  | Frames de arena con trinket, racial y categorías de DR por enemigo                                                        |
| **MiniCC**           | CC gigante en frames, tracking de CDs enemigos (kicks, ofensivos), alerta de "tu healer está en CC"                       |
| **FrameSort**        | Orden fijo de party1/party2 entre rondas — sin él, tus macros @party1/@party2 son ruleta rusa en Shuffle                   |

Atajo: el addon **Skill Capped UI** auto-configura todo el stack en un clic (ver `02-configuracion/addons_ui_programas.md`).




### 0.3 Macros mínimas (las 11 innegociables)

> ⚠️ Actualizado 2026-07-12: el set completo con código copiable, keybinds sugeridos y drill de automatización está en `02-configuracion/macros_resto_druid.md`. Ojo: **Resto NO tiene Mighty Bash en Midnight** — tu stun real es Rake desde Prowl (fuera de combate) y Maim (en combate, Cat Form).

Resumen del set: Nature's Cure `@party1`/`@party2` · Cyclone `@focus` y `@arena1/2/3` · Prowl+Rake (stun de apertura) · Maim (stun en combate) · Bear Form + Frenzied Regen en un botón · NS + Cyclone instantáneo · Trinket (`/use 14`) · Shadowmeld con `/stopcasting`. Ironbark `@party1`/`@party2` sube a obligatoria en Fase 1.

### 0.4 Keybinds

- Completa `02-configuracion/macros_y_ui.md`: ¿clicker o keybinder? Esto es lo primero que hay que saber. Si hay clicks en habilidades de reacción (trinket, Bark, kick en Cat), migrarlas a teclas ANTES de la Fase 1.
- Los dos botones laterales del mouse: **trinket** y **Cyclone @focus** son candidatos ideales (habilidades de reacción/presión).
- Regla: nada crítico en teclas que evites bajo presión.

**Ejercicio (sin colas):** 3 sesiones de 20 min contra dummies/duelos amistosos usando SOLO macros y keybinds nuevos hasta que salgan sin mirar la barra.

**Métrica de salida:** ✅ Build importado y verificado ✅ UI base configurada + stack de 3 addons funcionando (sArena Reloaded, MiniCC, FrameSort) ✅ 11 macros usadas sin pensar en un skirmish ✅ `02-configuracion/macros_y_ui.md` completado.

---



## FASE 1 — Fundamentos de sanación bajo presión (Semanas 3-5, ~24 h)

**Objetivo:** que sanar sea automático, para liberar cerebro para el juego ofensivo (Fase 2). No puedes pensar en Cyclone si aún piensas en Lifebloom.

### 1.1 Motor de sanación

- **Loop base:** Lifebloom permanente en quien recibe daño (el Apex *Everbloom* lo stackea hasta 3 — es tu principal fuente de output single-target), Rejuvenation en los 3, Regrowth como heal fuerte (buffado +40% este parche), Wild Growth con *Early Spring* instantáneo para procear Grove Guardians, Efflorescence donde pelea tu equipo.
- **Swiftmend + Nature's Swiftness:** son tus "botones de pánico" separados. Regla del parche: si un aliado baja de ~50% con burst encima y tienes NS disponible, úsalo — el error #1 detectado por análisis automático de logs en Resto Druids de Solo Shuffle es *dejar morir a un aliado con Nature's Swiftness disponible*.



### 1.2 Supervivencia (orden de trade defensivo)

1. Posicionamiento/pilar (gratis) → 2. Barkskin (ahora 30% DR, no lo guardes de más) → 3. Bear Form + Frenzied Regen → 4. Ironbark si el go es sobre un aliado → 5. Trinket solo si el CC conecta con el kill window enemigo.

- **Regla de trinket (tu duda declarada):** trinketea si (a) estás en CC completo Y (b) un aliado o tú está bajo 60% Y (c) los CDs ofensivos enemigos están activos. Si falta una de las tres, come el CC.



### 1.3 Maná

- En S1, la guerra de maná se gana con eficiencia (Regrowth solo con procs de Omen of Clarity, no spamear Rejuv en overheal) y bebiendo tras pilares en las transiciones. *(Sección a reescribir en 12.1 por el rework de Innervate.)*



### 1.4 Posicionamiento (inicio — se profundiza en Fase 2)

- Regla de max range: si un melee enemigo puede tocarte sin usar gap closer, estás mal parado.
- Un pilar siempre a ≤5 seg de tu posición.

**Laboratorio Solo Shuffle (2 sesiones/semana de 6 rondas):** una sesión enfocada SOLO en no morir + HoT upkeep; otra enfocada SOLO en trades defensivos correctos. Un foco por sesión — es entrenamiento de gimnasio, no partido.

**Métrica de salida:** ✅ 3 sesiones seguidas de Shuffle sin morir con Bark+Bear disponibles ✅ 0 muertes de aliados con NS sin usar en la sesión ✅ Trinket usado solo bajo la regla de las 3 condiciones (revisar mentalmente post-ronda) ✅ Rating de Shuffle estable o subiendo desde 1784.

---



## FASE 2 — Juego ofensivo: tu prioridad #1 (Semanas 6-9, ~32 h; cruza el inicio de S2)

**Objetivo:** convertirte de healer reactivo a playmaker. Aquí está la diferencia entre 1750 y 1950.

### 2.1 El sistema de DR de Midnight (apréndelo primero, todo lo demás depende de esto)

- **2 aplicaciones de CC de la misma categoría → inmunidad** (era 3 en expansiones anteriores). Reset: 16 seg en S1, **20 seg desde 12.1**.
- Consecuencia práctica: cada Cyclone vale el doble. Un Cyclone "para molestar" en mal momento regala la inmunidad que tu equipo necesitaba en el kill window.
- Ejercicio mental por partida: antes de lanzar CC, pregunta "¿esto abre un kill o solo gasta el DR?"



### 2.2 Cyclone — árbol de decisión

- **Cuándo es seguro hardcastear:** (a) el kick del melee que te presiona está en CD (míralo en MiniCC u OmniBar), (b) estás fuera de línea del caster con interrupt, o (c) tienes *Nature's Swiftness* para hacerlo instantáneo (el build estándar lo permite vía PvP talent — clave con tu latencia).
- **Objetivos por situación:** healer enemigo durante el go de tus DPS (el uso #1); DPS enemigo con CDs ofensivos activos durante SU go (Cyclone defensivo — inmuniza y anula su ventana); target a punto de recibir sanación grande.
- **Tu latencia (192-201 ms) importa:** el enemigo ve tu cast ~0.2 seg tarde y tú ves su kick tarde. Traducción: con kick enemigo disponible, NO hardcastees Cyclone en su línea de visión — usa NS o castea desde posición donde el kicker no te ve. Reserva los hardcasts para cuando contaste el kick.



### 2.3 Fake casting con 200 ms

- Tu fake debe cortarse ANTES de lo que tu instinto dice (el enemigo reacciona a información vieja tuya). Drill: en skirmish/Shuffle, dedica rondas a fakear Cyclone/Regrowth contra melees hasta sacar 2 kicks por ronda sin ser interrumpido.
- Cuenta los kicks enemigos en voz alta (literalmente): "kick del Warrior usado, 15 seg". MiniCC te lo muestra, pero verbalizar construye el hábito para cuando cantees en Discord.



### 2.4 Cadena ofensiva completa (el "go" de un Resto Druid)

Secuencia modelo cuando tus DPS abren CDs: **stun al healer enemigo (Rake desde Prowl si estás fuera de combate, Maim con combos si ya estás en pelea) → 1 Cyclone al healer (queda inmune a stun+cyclone, pero ya comió 6+ seg) → Roots al peel melee → seguir sanando**. La guía de Icy Veins lo resume así: CC constante sobre el healer enemigo mientras tus DPS burstean = el healer rival no llega y quema maná.

### 2.5 Posicionamiento anti-CC (tu error recurrente declarado)

- Causa raíz habitual: pararse en línea recta detrás del propio equipo → el mage/priest te alcanza con CC sin moverse. Corrección: **triángulo** — tú en un vértice con pilar cerca, nunca en la línea de visión natural del CCer enemigo.
- Drill de VOD (ver Fase 4): en cada CC que comas, pausa y pregunta "¿qué me llevó a estar visible para ese cast?"

**Laboratorio Solo Shuffle (foco único por sesión):**

- Sesión A: solo landing de Cyclone (meta: 3 Cyclones útiles por ronda, 0 en DR desperdiciado).
- Sesión B: solo fake cast y conteo de kicks.
- Sesión C: solo posicionamiento (meta: ≤1 CC completo comido por ronda sin trinket forzado).

**Métrica de salida:** ✅ Puedes decir en voz alta el estado de DR del healer enemigo en cualquier momento ✅ 3+ Cyclones que habilitaron presión real por ronda de Shuffle ✅ ≤1 interrupción sufrida por ronda en promedio ✅ Rating de Shuffle 1850+ (desde 1784).

---



## FASE 3 — Equipo, comps y comunicación (Semanas 10-13, ~32 h; ya en Season 2)

**Objetivo:** completar la transición solo → equipo coordinado. Es tu cuello de botella declarado y donde el 3v3 real se decide.

### 3.1 Comps objetivo (datos de S1 — revalidar al inicio de S2)

- **Resto Druid + Arms Warrior + Balance Druid** — la de mayor win rate del spec en S1 (72.6% en datos de ladder). Presión constante + doble raíz/cyclone.
- **Resto Druid + Balance Druid + BM Hunter** (67.6%) — daño instantáneo, no depende de casts.
- **Resto Druid + Survival Hunter + Shadow Priest** (61%).
- Patrón general: Resto Druid brilla en comps de **presión sostenida + cross-CC**, no en burst de setup puro. Busca DPS que entiendan que tu Cyclone ES parte del daño del equipo.



### 3.2 Dónde y cómo encontrar equipo (tu situación: LFG sin resultados)

- LFG in-game es lotería. Mejores canales: comunidades de Discord de PvP de tu región/idioma (busca comunidades hispanas de arena), el Discord de tu servidor/hermandades con núcleo PvP, y jugadores que se repiten en tus lobbies de Shuffle con buen nivel — susúrrales después de la partida.
- **Señales de un compañero que vale la pena:** (1) comunica sin tiltearse tras derrotas, (2) habla de SUS errores y no solo de los tuyos, (3) disponibilidad compatible con tus fines de semana, (4) acepta jugar 20-30 partidas antes de juzgar la comp. Rating actual importa menos que trayectoria.
- Meta concreta: **1 tarde de "citas" por semana** — probar 1 dúo/trío nuevo por sesión de fin de semana hasta fijar equipo.



### 3.3 Protocolo de comunicación (tu script mínimo)

Lo que TÚ canteas (corto, siempre igual):

- "Estoy en CC [tipo]" / "Trinket usado" / "Sin trinket el [enemigo]"
- "Voy Cyclone al healer en 3… 2… go" (avisa ANTES de castear, no después)
- "Kick del [X] usado" / "Necesito peel" / "Bebiendo, aguanten 5"

Lo que EXIGES de tus DPS:

- Anunciar su go 3-5 seg antes (para que tú prepares Bash/Cyclone)
- Estado de kicks/stuns propios ("tengo stun para el swap")
- Target de kill claro y anunciado en cada swap



### 3.4 Matchups (guías por arquetipo — pide el desglose completo en el chat cuando llegues aquí)

- **Melee cleave:** *Thorns*, jugar cerca de pilares, Bear Form temprano, no gastar trinket en el primer stun.
- **Caster cleave:** max range agresivo, *Disentanglement* si hay slows, forzar sus casts con presencia de Cyclone.
- **Rogue/Mage:** el matchup más difícil del spec según datos de S1 (Sub Rogue es tu peor enemigo estadístico). Trinket disciplinado, posicionamiento preventivo pre-opener, y comunicar "opener en mí" al instante.

**Métrica de salida:** ✅ Equipo fijo con el que jugaste 2 fines de semana completos ✅ Protocolo de comunicación usado en el 100% de las partidas (grábate y verifica) ✅ 30+ partidas de 3v3 puntuado con la misma comp ✅ Rating 3v3 de S2 en 1600+ y subiendo.

---



## FASE 4 — Mejora sostenida y push a récords (Semana 14 en adelante, continuo)

**Objetivo:** superar 1750 en 3v3 (meta 1950+) y 2100 en RBG (meta 2200+) con un sistema, no con grinding ciego.

### 4.1 Revisión de VODs

- **Grabación:** OBS con replay buffer (o la grabación de Windows) — solo partidas puntuadas.
- **Frecuencia:** 2 partidas revisadas por semana (1 derrota cerrada + 1 victoria). Más es procrastinación disfrazada de estudio.
- **Qué buscar según fase del error:** cada CC que comiste (¿posicionamiento?), cada muerte de aliado (¿NS/Ironbark disponibles?), cada Cyclone (¿abrió algo o quemó DR?), cada trinket (¿regla de 3 condiciones?).
- Registrar hallazgos en `04-seguimiento/registro_temporada.md` — el análisis de patrones cada 2-3 semanas se hace en el chat de Tracking.



### 4.2 Gestión mental (integrado con tu protocolo existente)

- Regla de 3 derrotas seguidas → parar (ya la tienes). Añadido: la revisión post-racha cuenta como sesión de entrenamiento, no como tiempo perdido.
- Las sesiones de Shuffle con foco único (Fases 1-2) son inmunes a la regla — son laboratorio, el rating ahí es termómetro, no objetivo.
- Con 8 h/semana: máximo 5-6 h de colas puntuadas; reserva 2 h para VOD + drills. La proporción jugador promedio es 100/0; la de los que suben es 75/25.



### 4.3 RBG (tu bracket fuerte — mantenimiento, no reconstrucción)

- Tus fundamentos de 2100 siguen ahí. Lo nuevo a validar en S2: build RBG específico (Murlok.io tiene página separada de RBG), y el rol de healer de FC se beneficia directamente de todo lo de la Fase 2 (posicionamiento anti-CC es supervivencia de FC).
- Push de RBG en paralelo desde S2 con comunidades organizadas (mismos canales que 3.2) — no random LFG a 2100+.

**Métrica de fase (rolling):** ✅ 2 VODs/semana revisados con notas ✅ Tendencia de rating positiva en ventanas de 3 semanas ✅ Hitos de `04-seguimiento/registro_temporada.md` tachándose.

---



## Tabla resumen


| Fase                          | Semanas | Objetivo central                              | Métrica de salida                                                                           |
| ----------------------------- | ------- | --------------------------------------------- | ------------------------------------------------------------------------------------------- |
| **0 — Cimientos técnicos**    | 1-2     | UI base, addons, macros, keybinds, build      | 11 macros automáticas en skirmish; UI completa; `02-configuracion/macros_y_ui.md` lleno                      |
| **1 — Sanación bajo presión** | 3-5     | Healing y defensivos automáticos              | 0 muertes con NS disponible; trinket solo con regla de 3 condiciones; Shuffle estable ≥1784 |
| **2 — Juego ofensivo** ⭐      | 6-9     | Cyclone, DR, fake cast, posicionamiento       | 3+ Cyclones útiles/ronda; ≤1 kick sufrido/ronda; Shuffle 1850+                              |
| **3 — Equipo y comps**        | 10-13   | Transición a 3v3 coordinado en S2             | Equipo fijo, 30+ partidas misma comp, protocolo de voz al 100%, 3v3 1600+                   |
| **4 — Push sostenido**        | 14+     | Superar 1750 → 1950 (3v3) y 2100 → 2200 (RBG) | 2 VODs/semana; tendencia positiva por trimestre                                             |


---



## Fuentes consultadas (2026-07-11)

- Icy Veins — Restoration Druid PvP Guide 12.0.7 (Mysticall, multi-R1): [https://www.icy-veins.com/wow/restoration-druid-pvp-guide](https://www.icy-veins.com/wow/restoration-druid-pvp-guide)
- Skill Capped — Resto Druid Talents & Builds S1 / Cambios 12.1: [https://www.skill-capped.com/wowarticles/guides/restoration-druid-pvp-guide/](https://www.skill-capped.com/wowarticles/guides/restoration-druid-pvp-guide/)
- Murlok.io — Resto Druid 3v3 y RBG (datos live top 50): [https://murlok.io/druid/restoration/3v3](https://murlok.io/druid/restoration/3v3)
- ArenaCoach — Resto Druid S1 (win rates, comps, errores comunes): [https://arenacoach.gg/guides/restoration-druid-pvp-guide-midnight-season-1](https://arenacoach.gg/guides/restoration-druid-pvp-guide-midnight-season-1)
- Icy Veins — 12.1 PTR Development Notes (DR, rework de Resto): [https://www.icy-veins.com/wow/news/massive-class-changes-midnight-12-1-curse-of-ulatek-development-notes/](https://www.icy-veins.com/wow/news/massive-class-changes-midnight-12-1-curse-of-ulatek-development-notes/)

*Distinción de tipo de consejo: builds/stats/comps = meta estadístico (datos de ladder, caducan con parches). Reglas de trinket, árbol de decisión de Cyclone, protocolo de comunicación = consejo situacional (estable entre parches).*