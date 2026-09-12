# Roadmap de Entrenamiento — Resto Druid PvP (Midnight)

> Generado: 2026-07-11 | **Recalendarizado: 2026-09-11** | Parche verificado: **12.1, Midnight Season 2**
> Season 2 en curso desde el 18 de agosto de 2026.
> Fuentes principales: Icy Veins PvP (Mysticall, multi-R1), Skill Capped, Murlok.io (datos live top 50), hotfixes oficiales de Blizzard (1 de septiembre de 2026).

---

## 📍 Dónde estás realmente (2026-09-11)

El plan original asumía cerrar Fases 0-1 durante S1 y empujar rating en S2. **Eso no ocurrió:** llevas ~380 partidas jugadas en Season 2 y sigues en Fase 0 — sin addons, sin macros, clickeando.


| Bracket            | Rating S2             | Partidas    | Win rate | Lectura                                                                |
| ------------------ | --------------------- | ----------- | -------- | ---------------------------------------------------------------------- |
| Solo Shuffle       | 1094 (era 1784 en S1) | 328 rondas  | **52%**  | La caída es el **reset de S2**, no pérdida de nivel. Subes, pero lento |
| Battleground Blitz | 1421 (era 1670 en S1) | 52 partidas | **38%**  | ⚠️ El único bracket bajo 50%. **Aquí está el problema real**           |


**El diagnóstico honesto:** 380 partidas de experiencia no se convierten en rating mientras juegues sin las herramientas. Un healer clicker sin frames de arena no puede dispelear a tiempo, no ve el DR enemigo y no reacciona a swaps. Eso no se arregla jugando más — se arregla en una tarde de configuración.

**La jugada correcta ahora:**

- **Semana 1 (esta):** cerrar Fase 0 completa. Addons + macros en español + paso 0 de la migración (girar con mouse). Cero puntuado serio.
- **Semanas 2-4:** Fase 1 con el rating de Shuffle como termómetro. El objetivo es recuperar 1784, no batir récords.
- **Semana 5 en adelante:** Fase 2 (tu prioridad #1 declarada) y push real.

> **Sobre el Blitz al 38%:** no lo ataques todavía. Blitz es 8v8 con presión constante y castiga más que Shuffle la falta de herramientas. Vuelve a él con la UI montada — la hipótesis es que ese número sube solo.

---



## ⚠️ Qué cambió con 12.1 (revalidado el 2026-09-11)

**Confirmado sin cambios** — tu build base sigue siendo correcto:

- **Keeper of the Grove** (42/50 de los top) · **Night Elf** (50/50) · tríada **Forest Guardian** (50/50) + **Early Spring** (48/50) + **Call of Ohn'ahra** (35/50) · stats de arena **Mastery > Versatility > Haste > Crit**.

**Lo que sí cambió:**

- **DR reset: 16 → 20 segundos.** Los goes se espacian más. *(Detalle en* `fase2_juego_ofensivo.md`*.)*
- **Innervate rediseñado:** ya no da hechizos gratis; regenera **20% del maná máximo en 8 seg** en PvP (el tooltip dice 25%; el hotfix del 1 de septiembre lo bajó a 20%). *(Detalle en* `fase1_sanacion_bajo_presion.md` *§3.)*
- **Nerfs del 1 de septiembre:** Swiftmend −20% en PvP, Regrowth −20%, sanación general −5%, Incarnation acortado. **El parche castiga al healer reactivo y premia al preventivo.**
- **Talentos:** *Overgrowth* nuevo (25/50, candidato real) · *Flash of Clarity* nuevo (0/50, ignóralo) · *Nature's Splendor* eliminado · *Abundance* rediseñado · *Typhoon* slow 50% → 30% (pero subió a 41/50) · *Ursol's Vortex* saltó a 43/50.
- **Ancient of Lore regresó como PvP talent pero el ladder no lo juega (3/50).** Icy Veins lo recomienda; los datos dicen que no. No hagas ese swap.
- **Stats por bracket:** en **Blitz/RBG el orden se invierte** — Versatility antes que Mastery.
- **Lo que NO caduca:** todo lo mecánico — posicionamiento, fake casting, lectura de DR, comunicación, hábitos. Ese es el 80% del roadmap y sigue intacto.

---



## ✅ FASE 0 — COMPLETADA el 2026-09-12

> **Cerrada en dos sesiones.** 0.1 build revalidado · 0.2 addons instalados y verificados · 0.3 macros (11 obligatorias + 6 opcionales, todas probadas) · 0.4 keybinds (12/12, giro con teclado desbindeado).
>
> **Único pendiente:** construir el hábito de *mouse turning* con práctica. No es configuración — es repetición.
>
> **Línea base antes de Fase 0** (para medir la mejora): Solo Shuffle ~1110 · Blitz ~1400 · iLvl 338. Todos esos números se lograron sin herramientas.

---

## FASE 0 — Cimientos técnicos (referencia)

**Objetivo:** dejar de jugar con desventaja de herramientas. Hoy juegas sin addons y sin macros: es como ir al gimnasio en sandalias. Antes de entrenar técnica, necesitas el equipo.

> 📌 **Recalendarizado el 2026-09-11:** el plan original daba 2 semanas y ~16 h a esta fase. Es una sobreestimación que la volvió fácil de aplazar — y llevas dos meses aplazándola. **El trabajo real son ~4 horas:** 30 min de addons, 40 min de macros, 30 min del paso 0 de keybinds, 15 min de verificación en skirmish, y ~1 h de drills. Cabe en un fin de semana.
>
> **Esta fase no tiene archivo propio** (a diferencia de las Fases 1 y 2): es este índice, y el detalle vive en los tres archivos de `02-configuracion/`. La ruta de aplicación paso a paso está abajo, en cada subsección.



### 0.1 Build y gear (verificar contra fuentes vivas, no memorizar)

- **Talentos y PvP talents:** ✅ **revalidado el 2026-09-11 para S2** — la tríada sigue siendo *Forest Guardian* (50/50), *Early Spring* (48/50) y *Call of Ohn'ahra* (35/50). Importa el build estándar de Skill Capped **creando un loadout nuevo de S2, no parcheando el viejo** (12.1 eliminó *Nature's Splendor* y añadió *Overgrowth* / *Flash of Clarity*). PvP talents situacionales a tener aprendidos: *Thorns* (vs doble melee), *Disentanglement* (vs comps con slows), *High Winds* (Cyclone defensivo vs equipos sin kicks). **No tomes *Ancient of Lore*** pese a que Icy Veins lo recomiende: 3/50 en el ladder.
- **Hero Talent:** ✅ *Keeper of the Grove* **revalidado el 2026-09-11 para S2: 42/50 de los top de 3v3 lo usan** (Wildstalker solo 8/50). Sigue siendo el correcto — no lo cambies. ⚠️ Ojo: las guías de **PvE** de 12.1 recomiendan Wildstalker; eso no aplica a PvP.
- **Stats:** **arena** = Mastery (38%) > Versatility (15%) > Haste (12%) > Crit (5%). ⚠️ **Blitz/RBG invierten el orden: Versatility > Mastery.** Juegas ambos brackets: si empujas Blitz en serio, es otro set de gemas/enchants. Copia los más usados en Murlok.io del bracket correspondiente — no teorices, son datos vivos.
- **Omnium Folio:** completar la cadena de misiones y elegir las runas PvP recomendadas en la página de builds de Icy Veins.
- **iLvl:** ⚠️ el 298 es dato de julio (S1). **Season 2 trajo gear nuevo y reseteó Conquest** — reverifica tu iLvl actual y capea el gear PvP semanal. Empujar rating con desventaja de iLvl es entrenar frustración.



### 0.2 UI base + addons (instalación mínima viable — una sesión de ~1 hora)

> ⚠️ Actualizado 2026-07-12: la lista original (Gladius/OmniBar/BigDebuffs/OmniCC/WeakAuras) quedó obsoleta por el "Addon Apocalypse" de Midnight — WeakAuras está muerto en retail y OmniCC es innecesario. El detalle completo, la configuración de la UI base y el orden de instalación están en `02-configuracion/addons_ui_programas.md`.

**Primero la UI base de Blizzard** (Cooldown Manager, números de CD nativos, cast bars en nameplates, DR nativo en frames de arena), **después el stack de 3 addons:**


| Addon            | Para qué                                                                                                 |
| ---------------- | -------------------------------------------------------------------------------------------------------- |
| **sArena Reloaded** | Frames de arena con trinket, racial y categorías de DR por enemigo                                       |
| **MiniAuras**       | CC gigante en frames, tracking de CDs enemigos (kicks, ofensivos), alerta de "tu healer está en CC"      |
| **FrameSort**    | Orden fijo de party1/party2 entre rondas — sin él, tus macros @party1/@party2 son ruleta rusa en Shuffle |


Atajo: el addon **Skill Capped UI** auto-configura todo el stack en un clic (ver `02-configuracion/addons_ui_programas.md`).

### 0.3 Macros mínimas (las 11 innegociables)

> 🔴 **CRÍTICO — tu cliente está en español.** Las macros deben llevar los **nombres de hechizo en español** (`/cast [@focus] Ciclón`, no `Cyclone`) o **no funcionan: se crean sin error y no hacen nada.** El set completo ya traducido, con glosario EN→ES y código copiable, está en `02-configuracion/macros_resto_druid.md`.
>
> **Método obligatorio: Shift+clic**, no tecleo. El cliente esES falla con los acentos según el teclado. Abre el grimorio (`P`), pon el cursor donde va el nombre y haz Shift+clic sobre el hechizo: el juego escribe el nombre exacto. **Ícono "?" al terminar = macro rota.**
>
> Ojo: **Resto NO tiene Mighty Bash en Midnight** — tu stun real es Rake desde Prowl (fuera de combate) y Maim (en combate, Cat Form).

Resumen del set: Nature's Cure `@party1`/`@party2` · Cyclone `@focus` y `@arena1/2/3` · Prowl+Rake (stun de apertura) · Maim (stun en combate) · Bear Form + Frenzied Regen en un botón · NS + Cyclone instantáneo · Trinket (`/use 14`) · Shadowmeld con `/stopcasting`. Ironbark `@party1`/`@party2` sube a obligatoria en Fase 1.

### 0.4 Keybinds

- ✅ Dato ya recogido: **eres clicker** (todo en barras, curas en 1-5, defensivos en barra 2, dispel en scroll abajo). El plan de migración incremental de 7 pasos está en `02-configuracion/macros_y_ui.md`.
- **Paso 0, el que bloquea todo lo demás: girar con el mouse (botón derecho sostenido), no con A/D.** Es el cambio más incómodo y el más importante: el giro con teclado tiene velocidad fija y lenta — en arena no llegas a kitear ni a reaccionar a swaps. Al hacerlo, A/D quedan libres como teclas de habilidad premium.
- ⚠️ **Q/E se conservan como strafe** (hábito de años). Donde una tabla sugiera Q o E para habilidades, usa **A/D**.
- Los dos botones laterales del mouse: **trinket** y **Cyclone @focus** (habilidades de reacción pura).
- Regla: nada crítico en teclas que evites bajo presión. Anótalas en `macros_y_ui.md` a medida que aparezcan en los drills.

**Ejercicio (sin colas):** las 4 sesiones del drill de `02-configuracion/macros_resto_druid.md` — empezando por la **sesión 0: verificación de idioma** (crear las 11 macros y confirmar que ninguna quedó con ícono "?").

**Métrica de salida:** ✅ Build de S2 importado como loadout nuevo ✅ UI base configurada + stack de addons funcionando (sArena Reloaded, MiniAuras, FrameSort) ✅ **11 macros creadas en español, 0 con ícono "?"** ✅ 11 macros usadas sin pensar en un skirmish ✅ Paso 0 de la migración hecho (giro con mouse) + trinket y Cyclone @focus en los laterales ✅ `02-configuracion/macros_y_ui.md` actualizado.

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

- La guerra de maná se gana con eficiencia (Regrowth solo con procs de Omen of Clarity, no spamear Rejuv en overheal) y bebiendo tras pilares en las transiciones. **En S2, Innervate es un "chupito de maná" (20% en 8 seg): úsalo al 50-60% de maná, no al 90% ni al 20%.** → desarrollo completo en `01-plan/fase1_sanacion_bajo_presion.md` §3.



### 1.4 Posicionamiento (inicio — se profundiza en Fase 2)

- Regla de max range: si un melee enemigo puede tocarte sin usar gap closer, estás mal parado.
- Un pilar siempre a ≤5 seg de tu posición.

**Laboratorio Solo Shuffle (2 sesiones/semana de 6 rondas):** una sesión enfocada SOLO en no morir + HoT upkeep; otra enfocada SOLO en trades defensivos correctos. Un foco por sesión — es entrenamiento de gimnasio, no partido.

**Métrica de salida:** ✅ 3 sesiones seguidas de Shuffle sin morir con Bark+Bear disponibles ✅ 0 muertes de aliados con NS sin usar en la sesión ✅ Trinket usado solo bajo la regla de las 3 condiciones (revisar mentalmente post-ronda) ✅ Rating de Shuffle estable o subiendo desde 1784.

---



## FASE 2 — Juego ofensivo: tu prioridad #1 (Semanas 6-9, ~32 h; cruza el inicio de S2)

**Objetivo:** convertirte de healer reactivo a playmaker. Aquí está la diferencia entre 1750 y 1950.

### 2.1 El sistema de DR de Midnight (apréndelo primero, todo lo demás depende de esto)

- **2 aplicaciones de CC de la misma categoría → inmunidad** (era 3 en expansiones anteriores). Reset: **20 segundos** (era 16 en S1).
- Consecuencia práctica: cada Cyclone vale el doble. Un Cyclone "para molestar" en mal momento regala la inmunidad que tu equipo necesitaba en el kill window.
- Ejercicio mental por partida: antes de lanzar CC, pregunta "¿esto abre un kill o solo gasta el DR?"



### 2.2 Cyclone — árbol de decisión

- **Cuándo es seguro hardcastear:** (a) el kick del melee que te presiona está en CD (míralo en MiniAuras u OmniBar), (b) estás fuera de línea del caster con interrupt, o (c) tienes *Nature's Swiftness* para hacerlo instantáneo (el build estándar lo permite vía PvP talent — clave con tu latencia).
- **Objetivos por situación:** healer enemigo durante el go de tus DPS (el uso #1); DPS enemigo con CDs ofensivos activos durante SU go (Cyclone defensivo — inmuniza y anula su ventana); target a punto de recibir sanación grande.
- **Tu latencia (192-201 ms) importa:** el enemigo ve tu cast ~0.2 seg tarde y tú ves su kick tarde. Traducción: con kick enemigo disponible, NO hardcastees Cyclone en su línea de visión — usa NS o castea desde posición donde el kicker no te ve. Reserva los hardcasts para cuando contaste el kick.



### 2.3 Fake casting con 200 ms

- Tu fake debe cortarse ANTES de lo que tu instinto dice (el enemigo reacciona a información vieja tuya). Drill: en skirmish/Shuffle, dedica rondas a fakear Cyclone/Regrowth contra melees hasta sacar 2 kicks por ronda sin ser interrumpido.
- Cuenta los kicks enemigos en voz alta (literalmente): "kick del Warrior usado, 15 seg". MiniAuras te lo muestra, pero verbalizar construye el hábito para cuando cantees en Discord.



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

### 3.1 Comps objetivo (✅ revalidadas para S2 el 2026-09-11)

- **Resto Druid + Balance Druid + BM Hunter** — **la de mayor win rate del spec en S2 (77,5% sobre 245 partidas)**. Daño instantáneo que no depende de casts: perfecto para tu latencia, porque tus compañeros no pierden output por ping.
- **Resto Druid + Arms Warrior + Balance Druid** — la #1 de S1 (72,6%), sigue siendo sólida. Presión constante + doble raíz/cyclone.
- **Resto Druid + Affliction Warlock + Frost Mage** — fuerte en S2 según Skill Capped.
- Dato de contexto: Resto Druid tiene **78 comps distintas por encima del 50%** de win rate (puesto 7 de 36 specs). No te faltan opciones: te falta equipo.
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

- Anunciar su go 3-5 seg antes (para que tú prepares tu stun —Rake desde Prowl o Maim— y el Cyclone)
- Estado de kicks/stuns propios ("tengo stun para el swap")
- Target de kill claro y anunciado en cada swap



### 3.4 Matchups (guías por arquetipo — pide el desglose completo en el chat cuando llegues aquí)

- **Melee cleave:** *Thorns*, jugar cerca de pilares, Bear Form temprano, no gastar trinket en el primer stun.
- **Caster cleave:** max range agresivo, *Disentanglement* si hay slows, forzar sus casts con presencia de Cyclone.
- **Rogue/Mage:** el matchup más difícil del spec (Sub Rogue es tu peor enemigo estadístico). Trinket disciplinado, posicionamiento preventivo pre-opener, y comunicar "opener en mí" al instante. *(Dato de S1 — revalidar contra el ladder de S2 cuando llegues a esta fase.)*

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


| Fase                          | Semanas | Objetivo central                                 | Métrica de salida                                                                                       |
| ----------------------------- | ------- | ------------------------------------------------ | ------------------------------------------------------------------------------------------------------- |
| **0 — Cimientos técnicos**    | 1       | UI base, addons, macros **en español**, keybinds | 11 macros sin ícono "?" y automáticas en skirmish; UI completa; `02-configuracion/macros_y_ui.md` lleno |
| **1 — Sanación bajo presión** | 2-4     | Healing y defensivos automáticos                 | 0 muertes con NS disponible; trinket solo con regla de 3 condiciones; Shuffle recuperando hacia 1784    |
| **2 — Juego ofensivo** ⭐      | 5-8     | Cyclone, DR (20 seg), fake cast, posicionamiento | 3+ Cyclones útiles/ronda; ≤1 kick sufrido/ronda; Shuffle 1850+                                          |
| **3 — Equipo y comps**        | 9-12    | Transición a 3v3 coordinado                      | Equipo fijo, 30+ partidas misma comp, protocolo de voz al 100%, 3v3 1600+                               |
| **4 — Push sostenido**        | 13+     | Superar 1750 → 1950 (3v3) y 2100 → 2200 (RBG)    | 2 VODs/semana; tendencia positiva por trimestre                                                         |


> Las semanas son relativas al arranque real (2026-09-11), no a fechas de calendario. La Fase 0 bajó de 2 semanas a 1: son ~4 horas de trabajo, no dos semanas — llevas dos meses aplazándola.

---



## Fuentes consultadas

**Revalidación de S2 (2026-09-11):**

- Murlok.io — Resto Druid **3v3** (heatmap live, top 50, refresco cada 8 h): [https://murlok.io/druid/restoration/3v3](https://murlok.io/druid/restoration/3v3)
- Murlok.io — Resto Druid **Solo Shuffle** (tu bracket principal): [https://murlok.io/druid/restoration/solo](https://murlok.io/druid/restoration/solo)
- Murlok.io — Resto Druid **Battleground Blitz** (tu segundo bracket): [https://murlok.io/druid/restoration/blitz](https://murlok.io/druid/restoration/blitz)
- Murlok.io — Resto Druid **RBG** (de grupo): [https://murlok.io/druid/restoration/rbg](https://murlok.io/druid/restoration/rbg)
- Blizzard — **Hotfixes del 1 de septiembre de 2026** (nerfs de Swiftmend/Regrowth, Innervate al 20% en PvP): [https://news.blizzard.com/en-us/article/24296142/hotfixes-september-1-2026](https://news.blizzard.com/en-us/article/24296142/hotfixes-september-1-2026)
- Icy Veins — Restoration Druid PvP Guide 12.1 (Mysticall, multi-R1): [https://www.icy-veins.com/wow/restoration-druid-pvp-guide](https://www.icy-veins.com/wow/restoration-druid-pvp-guide)
- Skill Capped — Resto Druid: cambios de 12.1 y builds de S2: [https://www.skill-capped.com/wowarticles/guides/restoration-druid-pvp-guide/](https://www.skill-capped.com/wowarticles/guides/restoration-druid-pvp-guide/)
- Icy Veins — Notas de desarrollo 12.1 (DR 16→20 seg): [https://www.icy-veins.com/wow/news/class-changes-diminishing-returns-midnight-12-1-ptr-development-notes-june-30th/](https://www.icy-veins.com/wow/news/class-changes-diminishing-returns-midnight-12-1-ptr-development-notes-june-30th/)

**Consulta original (2026-07-11):**

- ArenaCoach — Resto Druid S1 (win rates, comps, errores comunes): [https://arenacoach.gg/guides/restoration-druid-pvp-guide-midnight-season-1](https://arenacoach.gg/guides/restoration-druid-pvp-guide-midnight-season-1)

*Distinción de tipo de consejo: builds/stats/comps = meta estadístico (datos de ladder, caducan con parches). Reglas de trinket, árbol de decisión de Cyclone, protocolo de comunicación = consejo situacional (estable entre parches).*