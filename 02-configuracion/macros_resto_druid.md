# Macros — Resto Druid PvP (Midnight S2, 12.1)

> Fuentes: Skill Capped (macros S1) e Icy Veins PvP (Mysticall). Verificado 2026-07-11. **Traducido a cliente esES el 2026-09-11.**
>
> **Cómo crearlas:** `ESC → Macros` (o `/macro`) → pestaña **"Específicas de personaje"** → Nueva → nombre corto → ícono **"?"** (con `#showtooltip` el ícono se actualiza solo) → pegar código → arrastrar a la barra de acción → asignar tecla en `ESC → Opciones → Asignación de teclas`.
>
> **Regla general:** las macros `@algo` lanzan el hechizo sobre ese objetivo SIN cambiar tu target. Ese es todo el punto: sigues viendo a tu equipo mientras controlas al enemigo.

---

## ⚠️ LEE ESTO ANTES DE ESCRIBIR UNA SOLA MACRO (cliente en español)

**Tu cliente es esES. Los nombres de hechizo en las macros DEBEN ir en español o la macro no hace nada** — no da error, no avisa: simplemente no funciona. Es el fallo más caro y silencioso de todos.

Tres reglas que se derivan de eso:

1. **Los comandos van en inglés, los hechizos en español.** `/cast`, `#showtooltip`, `/use`, `/stopcasting` son comandos: NUNCA se traducen. `Ciclón`, `Piel de corteza`, `Acechar` son nombres: SIEMPRE en español.
2. **Usa Shift+clic, no tecleo.** El cliente esES tiene un fallo conocido con los acentos: según tu teclado, escribir `Ciclón` a mano puede romper la macro aunque se vea idéntico. **Método a prueba de balas:** abre el grimorio (`P`), pon el cursor donde va el nombre dentro de la macro y haz **Shift+clic** sobre el hechizo — el juego escribe el nombre exacto, con el acento correcto. Hazlo así con TODOS los hechizos acentuados (Ciclón, Raíces enredaderas, Corazón de lo Salvaje).
3. **Ícono "?" = macro rota.** Si tras crear la macro el ícono se queda en el signo de interrogación en vez de mostrar el hechizo, el nombre está mal escrito. Es tu alarma instantánea, aprovéchala en cada macro que crees.

> Los nombres en inglés se conservan en este archivo entre paréntesis porque son los que usan Murlok, Icy Veins y Skill Capped. **Para leer guías, usa el inglés. Para escribir macros, usa el español.**

### Glosario EN → ES (los que necesitas para las macros)

| Inglés (guías) | Español (tu cliente) | ¿Acento? |
|---|---|---|
| Cyclone | **Ciclón** | ⚠️ Sí — Shift+clic |
| Nature's Cure | **Cura de la naturaleza** | No |
| Nature's Swiftness | **Presteza de la Naturaleza** | No |
| Swiftmend | **Alivio presto** | No |
| Ironbark | **Corteza de hierro** | No |
| Barkskin | **Piel de corteza** | No |
| Bear Form | **Forma de oso** | No |
| Cat Form | **Forma felina** | No |
| Frenzied Regeneration | **Regeneración frenética** | ⚠️ Sí — Shift+clic |
| Prowl | **Acechar** | No |
| Rake | **Arañazo** | ⚠️ Sí — Shift+clic |
| Maim | **Amputar** ⚠️ *(corregido 2026-09-12: el proyecto decía "Destripar", que es **Rip** — un sangrado, no un stun. Verificado in-game por el jugador)* | No |
| Rip | **Destripar** *(sangrado — NO es tu stun)* | No |
| Shadowmeld (racial) | **Fusión de las sombras** | ⚠️ Sí — Shift+clic |
| Entangling Roots | **Raíces enredaderas** | ⚠️ Sí — Shift+clic |
| Wild Charge | **Carga salvaje** | No |
| Efflorescence | **Floración** | ⚠️ Sí — Shift+clic |
| Rejuvenation | **Rejuvenecimiento** | No |
| Lifebloom | **Flor de vida** | No |
| Wild Growth | **Crecimiento salvaje** | No |
| Regrowth | **Recrecimiento** | No |
| Incapacitating Roar | **Rugido incapacitante** | No |
| Mass Entanglement | **Enredo masivo** | No |
| Ursol's Vortex | **Vórtice de Ursol** | ⚠️ Sí — Shift+clic |
| Typhoon | **Tifón** | ⚠️ Sí — Shift+clic |
| Stampeding Roar | **Rugido de estampida** | No |
| Innervate | **Estimular** | No |
| Tranquility | **Tranquilidad** | No |
| Incarnation: Tree of Life | **Encarnación: Árbol de vida** | ⚠️ Sí — Shift+clic |
| Grove Guardians | **Fuerza de la Naturaleza** | No |
| Omen of Clarity | **Augurio de claridad** | No |
| Heart of the Wild | **Corazón de lo Salvaje** | ⚠️ Sí — Shift+clic |

> ⚠️ **Verifica cada nombre con el tooltip in-game antes de darlo por bueno.** Estas traducciones vienen de fuentes de la comunidad; Midnight rediseñó parte del kit y Blizzard a veces retraduce. La regla de precedencia del proyecto aplica igual aquí: **gana el tooltip**. El método Shift+clic te inmuniza contra esto — el juego siempre escribe el nombre correcto.



## OBLIGATORIAS (11) — sin esto no se cierra la Fase 0


| #   | Macro                                  | Código (⚠️ nombres en ESPAÑOL — cliente esES)                                                                                            | Qué hace                                                                                                                                          | Cuándo usarla                                                                                              | Por qué tenerla                                                                                                                                                        |
| --- | -------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1   | **Nature's Cure @party1** (Cura de la naturaleza) | `#showtooltip` `/cast [@party1] Cura de la naturaleza`                                                                        | Disipa al aliado 1 sin seleccionarlo                                                                                                              | Al instante de ver CC mágico o debuff clave en el frame                                                    | Dispel tardío = sanación desperdiciada. Un Poly disipado en 0.5 seg vs 2 seg cambia la partida                                                                         |
| 2   | **Nature's Cure @party2** (Cura de la naturaleza) | `#showtooltip` `/cast [@party2] Cura de la naturaleza`                                                                        | Igual, aliado 2                                                                                                                                   | Igual                                                                                                      | Igual                                                                                                                                                                  |
| 3   | **Cyclone @focus** (Ciclón)            | `#showtooltip` `/cast [@focus] Ciclón` ⚠️ Shift+clic                                                                                     | Cyclone al focus (normalmente el healer enemigo) sin soltar tu target                                                                             | Arranca el go de tus DPS → Cyclone al healer                                                               | LA macro de tu prioridad #1. Sin ella, ciclonear = cambiar target, perder visión del equipo, volver                                                                    |
| 4   | **Cyclone @arena1** (Ciclón)           | `#showtooltip` `/cast [@arena1] Ciclón` ⚠️ Shift+clic                                                                                    | Cyclone al enemigo 1 de los frames de arena                                                                                                       | Cuando el objetivo NO es tu focus (ej: Mage con Combustion)                                                | Control sobre los 3 enemigos sin tocar target ni focus                                                                                                                 |
| 5   | **Cyclone @arena2** (Ciclón)           | `#showtooltip` `/cast [@arena2] Ciclón` ⚠️ Shift+clic                                                                                    | Igual, enemigo 2                                                                                                                                  | Igual                                                                                                      | Si te satura al inicio, empieza solo con #3 y agrega 4-6 en semana 2                                                                                                   |
| 6   | **Cyclone @arena3** (Ciclón)           | `#showtooltip` `/cast [@arena3] Ciclón` ⚠️ Shift+clic                                                                                    | Igual, enemigo 3                                                                                                                                  | Igual                                                                                                      | Igual                                                                                                                                                                  |
| 7   | **Prowl + Rake (tu stun de apertura)** | ⚠️ **REESCRITA 2026-09-12** — ver §"Macro 7 corregida" abajo. La versión anterior alternaba forma felina/humana al pulsarla repetidamente | Cat Form → Prowl (sigilo) → Rake, que **desde sigilo aturde**. ⚠️ Resto NO tiene Mighty Bash en Midnight — este es tu stun real | Antes de abrir puertas o en transiciones fuera de combate: Prowl → Rake al healer enemigo → Cyclone encima | Es el opener estándar del spec según Icy Veins. Prowl requiere estar fuera de combate; en pelea tu stun es Maim (fila 7b)                                              |
| 7b  | **Maim (stun en combate)** (**Amputar**) | `#showtooltip` `/cast Amputar`                                                                                                         | Stun en melee que consume puntos de combo (1-5 seg según combos). ⚠️ **Corregido:** el proyecto decía "Destripar" — eso es **Rip**, un sangrado | En Cat Form pegado al objetivo: Rake/Shred generan combos → Maim aturde                                    | 49/50 de los top lo talentan. *Forest Guardian* (tu PvP talent) existe para esto: agredir en Cat sin que tus HoTs mueran. Jugada de Fase 2+, no la fuerces en semana 1 |
| 8   | **Bear + Frenzied Regen**              | `#showtooltip` `/cast [nostance] Forma de oso` `/cast [form:2] Forma de oso` `/cast [form:3] Forma de oso` `/cast [form:1] Regeneración frenética` ⚠️ Shift+clic | 1er toque = Bear Form (desde cualquier forma); 2do toque = Frenzied Regen                                                                         | El swap viene hacia ti y Barkskin no basta: spamea la tecla                                                | Bajo pánico no hay tiempo de "primero forma, luego heal". Un botón = capa defensiva 2 completa                                                                         |
| 9   | **NS + Cyclone instantáneo**           | `#showtooltip` `/cast Presteza de la Naturaleza` `/cast Ciclón` ⚠️ Shift+clic                                                            | Con *Call of Ohn'ahra*: Cyclone instantáneo, imposible de kickear                                                                                 | Momento clutch: kill window abierto, sin tiempo de hardcast                                                | Con tus 200 ms, el único Cyclone que tu ping no puede arruinar. Variante: última línea `/cast [@focus] Ciclón`                                                         |
| 10  | **Trinket PvP**                        | `#showtooltip` `/use 14`                                                                                                                 | Usa el accesorio del slot 14 (Medallion). Si está arriba, cambia a `/use 13`                                                                      | Solo con la regla de 3 condiciones (CC completo + aliado/tú <60% + CDs enemigos activos)                   | Trinket clickeado desde bolsa = trinket tarde. Tecla dedicada, siempre la misma. **Sin nombre de hechizo = inmune al idioma** |
| 11  | **Shadowmeld instantáneo**             | `#showtooltip` `/stopcasting` `/cast Fusión de las sombras` ⚠️ Shift+clic                                                                | Corta tu cast y te desvanece: pierden target sobre ti; casts dirigidos a ti fallan                                                                | Uso pro: el caster enemigo termina su CC hacia ti → Meld en el último instante → el cast se pierde         | Eres Night Elf: este racial es la razón por la que el 98% de los top lo son (50/50 en el top de 3v3 este parche). Sin macro no corta tu propio cast                    |




## 🚨 CÓMO PEGAR UNA MACRO (leer antes de copiar nada)

**Cada comando va en su propia línea.** En las tablas de abajo el código aparece en una sola celda por limitaciones del formato, pero al pegarlo en el juego hay que separarlo.

❌ **Mal** (todo pegado — la macro no funciona):
```
#showtooltip /cast [@arena1] Ciclón
```

✅ **Bien** (un comando por renglón):
```
#showtooltip
/cast [@arena1] Ciclón
```

> Esto causó que las macros 4/5/6 no funcionaran durante una sesión entera. Si una macro no hace nada y el nombre del hechizo es correcto, **revisa los saltos de línea primero**.

---

## 📋 Estado de implementación (probado in-game el 2026-09-12)

| # | Macro | Estado | Nota |
|---|---|---|---|
| 1 | Nature's Cure @party1 | ✅ **Implementada** | Funciona con mouseover sobre el marco, sin seleccionar |
| 2 | Nature's Cure @party2 | ✅ **Implementada** | Igual |
| 3 | Cyclone @focus | ✅ **Implementada** | Requiere tener un enemigo en focus (ver §Target vs Focus del glosario) |
| 4 | Cyclone @arena1 | ✅ **Implementada** | ⚠️ Falló al principio por pegarse sin saltos de línea |
| 5 | Cyclone @arena2 | ✅ **Implementada** | Igual |
| 6 | Cyclone @arena3 | ✅ **Implementada** | Igual |
| 7 | Prowl + Rake | ✅ **Implementada** | Funciona con la versión corregida (`!` + `form:2`). **Uso real: Fase 2+** — ver nota de utilidad abajo |
| 7b | Maim (**Amputar**) | ✅ **Implementada** | Requiere puntos de combo. **Uso real: Fase 2+** — ver nota de utilidad abajo |
| 8 | Bear + Frenzied Regen | ✅ **Implementada** | "Funciona perfectamente" |
| 9 | NS + Cyclone instantáneo | ✅ **Implementada** | |
| 10 | Trinket (`/use 14`) | ✅ **Implementada** | |
| 11 | Shadowmeld | ✅ **Implementada** | |
| **12** | **Focus @mouseover** | 🆕 **Pendiente de crear** | Faltaba en el set original: sin ella, fijar el focus es manual |

**Resumen: 11 de 11 creadas y funcionando.** ✅ **Fase 0.3 cerrada.**

> **Macro 12 (Focus @mouseover) descartada** el 2026-09-12: el jugador fija el focus con **clic derecho sobre el marco enemigo de sArena**, que es más rápido que cualquier macro. No hace falta.

### Estado de las macros OPCIONALES (probadas in-game el 2026-09-12)

| # | Macro | Estado | Nota del jugador |
|---|---|---|---|
| A | Ironbark @party1/@party2 | ✅ **Implementada** | "Útiles, funcionan correctamente" |
| B | NS + Regrowth (pánico) | ✅ **Implementada** | ⚠️ Compite por NS con la macro 9: NS tiene **una sola carga** |
| C | Entangling Roots @focus | ✅ **Implementada** | "Muy útil" |
| D | Wild Charge @party1/@party2 | ✅ **Implementada** | "Demasiado útil, y es una habilidad que no uso mucho" → **fuérzala conscientemente: es tu escape del tren melee y tu debilidad declarada es el posicionamiento** |
| E | ~~Efflorescence @cursor~~ | ❌ **No aplica** | Floración es automática en su build (ver fila E abajo) |
| F | Talento flexible AoE CC | ✅ **Implementada** | Pendiente de probar en partida |
| G | ~~Incapacitating Roar~~ | ⚪ **Innecesaria** | Idéntica al hechizo suelto — no aporta nada |
| H | Nature's Cure @mouseover | ✅ **Implementada** | La evolución del dispel en scroll abajo |

**6 de 8 opcionales útiles.** Las descartadas (E y G) lo son por diseño del juego, no por error de configuración.

### ⚠️ Utilidad real de las macros 7 y 7b (stuns)

Funcionan, pero **no son macros de Fase 0-1.** Conviene entender por qué antes de intentar usarlas en partida:

| Macro | Limitación | Cuándo sí compensa |
|---|---|---|
| **7 — Prowl + Rake** | Prowl (Acechar) exige estar **fuera de combate**. En Solo Shuffle las rondas arrancan con todos peleando: la ventana casi no existe | Solo antes de que abran las puertas, o si logras resetear combate tras un pilar. Exige salir de posición de healer y volver |
| **7b — Amputar** | Necesita **puntos de combo**, que se generan pegando en forma de gato. Para aturdir hay que dejar de curar primero | Cuando tus DPS anuncian un go: stun (4-5 seg) + Cyclone (6 seg) = ~10 seg sin sanación enemiga. Eso mata |

**Regla de seguridad (de `fase2_juego_ofensivo.md` §4, Cadena B):** solo entras en Cat Form con (a) HoTs completos en los 3, (b) sin go enemigo en curso, y (c) NS disponible como airbag. Si falta una, tu aporte al go es Cyclone a distancia y nada más.

> **En resumen:** de tus 12 macros, las dos de stun son las menos útiles hoy. Tu prioridad #1 declarada es el timing de Cyclone, y eso vive en las macros 3, 4, 5, 6 y 9. Déjalas creadas y no las fuerces hasta Fase 2.

---

## Macro 7 corregida (Prowl + Rake)

**Por qué fallaba la anterior:** `/cast [noform:1] Forma felina` intenta entrar en forma felina cuando NO estás en ella. Pero `Forma felina` es un *toggle*: si el juego evalúa mal el estado (o ya estás en gato), la vuelve a lanzar y te saca. De ahí el ciclo gato → humano → gato que observaste.

**Versión corregida** — usa `!` (fuerza la forma, nunca la quita) y `Acechar` también con `!`:

```
#showtooltip
/cast [nostealth,noform:2] !Forma felina
/cast [form:2,nostealth] !Acechar
/cast [stealth] Arañazo
```

> ⚠️ **`form:2` asume que Forma felina es tu segunda forma.** El número depende de qué formas tengas aprendidas. Si no funciona, prueba `form:1` o `form:3`. Comprobación rápida: escribe `/script print(GetShapeshiftForm())` en el chat estando en forma felina — te dice el número exacto.

**Cómo usarla:** tres pulsaciones sucesivas. 1ª → forma felina. 2ª → sigilo. 3ª → Arañazo (que desde sigilo aturde). El `!` impide que salgas de la forma por pulsar de más.

---

## Macro 12 — Focus @mouseover (nueva, obligatoria)

La macro 3 (Cyclone @focus) es tu herramienta principal, pero el set **no incluía ninguna forma rápida de poner el focus**. Sin esto tienes que seleccionar al enemigo, escribir `/focus`, y volver a seleccionar a tu aliado.

```
#showtooltip
/focus [@mouseover,harm,exists][]
```

**Cómo funciona:** pasas el cursor sobre el enemigo (en pantalla o en su marco de sArena) y pulsas la tecla. Queda fijado como focus **sin perder tu target actual**. Si no hay nadie bajo el cursor, pone en focus a tu objetivo actual.

**Keybind sugerido:** una tecla cómoda pero no crítica — el focus se pone una vez por ronda, no bajo presión. `Shift+F` o similar.

**Rutina de inicio de cada ronda:** identificar al healer enemigo → cursor encima → focus → ya no lo tocas. A partir de ahí tu macro 3 siempre apunta a él.

---

## OPCIONALES — agregar en semanas 2-4, en este orden


| #   | Macro                             | Código (⚠️ nombres en ESPAÑOL — cliente esES)                                                                    | Qué hace / Cuándo                                                                                               | Nota                                                                               |
| --- | --------------------------------- | ---------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| A   | **Ironbark @party1 / @party2** (Corteza de hierro) | `#showtooltip` `/cast [@party1] Corteza de hierro` *(duplicar para party2)*                     | Tu externo instantáneo al aliado, al inicio del go enemigo sobre él                                             | Sube a obligatoria en Fase 1. Opcional solo mientras te acostumbras al resto       |
| B   | **NS + Regrowth (pánico)**        | `#showtooltip` `/castsequence reset=3 Presteza de la Naturaleza, Recrecimiento`                                  | 1er toque NS, 2do Regrowth instantáneo (se reinicia a los 3 seg)                                                | ⚠️ Compite por NS con #9. NS es UNA carga: decide en el momento si es heal o CC    |
| C   | **Entangling Roots @focus** (Raíces enredaderas) | `#showtooltip` `/cast [@focus] Raíces enredaderas` ⚠️ Shift+clic                                   | Roots al focus: peel o separar al healer enemigo de su equipo                                                   | Versiones @arena123 si escalas                                                     |
| D   | **Wild Charge @party1 / @party2** (Carga salvaje) | `#showtooltip` `/cast [@party1] Carga salvaje` *(duplicar para party2)*                           | Vuelas hacia tu aliado: escape instantáneo del tren melee                                                       | Salvavidas lejos de pilares                                                        |
| E   | ~~**Efflorescence @cursor** (Floración)~~ | ❌ **NO APLICA a tu build** (verificado in-game 2026-09-12)                                              | En tu build Floración **se coloca sola** — no hay hechizo que lanzar, así que la macro no puede existir          | Causa probable: tienes el talento **Lifetreading**, que mueve Floración automáticamente bajo tu objetivo de Lifebloom. Si algún día lo sueltas, Floración vuelve a ser un hechizo de suelo y esta macro recupera sentido |
| F   | **Talento flexible: AoE CC**      | `#showtooltip` `/cast [known:Enredo masivo] Enredo masivo` `/cast [known:Vórtice de Ursol] Vórtice de Ursol` ⚠️ Shift+clic | Usa automáticamente el talento que tengas en esa fila                                              | A prueba de swaps de matchup (Fase 4): cambias talentos sin reorganizar barras. ⚠️ `known:` también necesita el nombre en español |
| G   | ~~**Incapacitating Roar**~~ (Rugido incapacitante) | ⚪ **INNECESARIA** (verificado 2026-09-12)                                                       | `/cast Rugido incapacitante` hace **exactamente lo mismo** que el botón del hechizo: es AoE alrededor de ti, no acepta `@objetivo` | Usa el hechizo directamente y ahorra el espacio de barra. Solo tendría sentido si alternaras el talento y quisieras un botón fijo con `#showtooltip` |
| H   | **Nature's Cure @mouseover** (Cura de la naturaleza) | `#showtooltip` `/cast [@mouseover,help,nodead][@target] Cura de la naturaleza`                 | Cursor sobre el frame del aliado + tecla = dispel a ESE aliado sin targetear. Sin mouseover, disipa a tu target | La evolución de tu scroll abajo — ver tabla de keybinds                            |




## Keybinds sugeridos (tu configuración: 2 botones laterales de mouse, dispel en scroll)

> ⚠️ Ajuste 2026-07-12: strafeas con Q/E — esas teclas se CONSERVAN como movimiento. Donde esta tabla diga Q o E, usa **A y D** (quedan libres al pasar el giro del personaje al mouse — ver plan de migración en `02-configuracion/macros_y_ui.md`). El resto de la tabla aplica igual.

**Tu scroll abajo: consérvalo, pero cámbiale el contenido por la macro H (@mouseover).** Si el cursor no está sobre nadie, se comporta idéntico a tu bind actual — upgrade sin costo de reaprendizaje.


| Tecla                   | Macro                                              | Razón                                            |
| ----------------------- | -------------------------------------------------- | ------------------------------------------------ |
| Scroll abajo            | H — Nature's Cure @mouseover                       | Tu hábito de años + mouseover gratis             |
| Mouse lateral frontal   | #3 — Cyclone @focus                                | Tu macro de presión más usada: acceso más rápido |
| Mouse lateral trasero   | #10 — Trinket                                      | Reacción pura, cero desplazamiento de dedos      |
| Shift+Scroll abajo      | #1 — Nature's Cure @party1                         | Respaldo cuando el cursor está ocupado           |
| Ctrl+Scroll abajo       | #2 — Nature's Cure @party2                         | Igual                                            |
| F                       | #8 — Bear+Frenzied                                 | La tecla de pánico más cómoda cerca de WASD      |
| Shift+F                 | #9 — NS+Cyclone                                    | Junto a su hermana defensiva                     |
| Q                       | #7 — Prowl+Rake (y Maim en Shift+R o tecla cómoda) | Reacción ofensiva, dedo índice                   |
| Shift+Q                 | C — Roots @focus                                   | Misma familia                                    |
| 4, 5, 6 (o Shift+1/2/3) | #4-6 — Cyclone @arena1/2/3                         | Planificadas, pueden vivir más lejos             |
| E / Shift+E             | A — Ironbark @party1/@party2                       | Externo = reacción, cerca de WASD                |
| V                       | #11 — Shadowmeld                                   | Accesible pero sin riesgo de toque accidental    |


**Principio:** reacción cerca de WASD (Q, E, R, F, C, V y Shift+); planificado puede vivir lejos. **Test:** si en un skirmish dudas qué tecla es, el bind está mal ubicado, no tu memoria.

## Drill de automatización (antes de colar nada)


| Sesión     | Dónde          | Contenido                                                                                                                               | Métrica                                 |
| ---------- | -------------- | --------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------- |
| 0 (10 min) | Cualquier sitio | **Verificación de idioma (nueva, obligatoria):** crear las 11 macros con Shift+clic y confirmar que NINGUNA quedó con ícono "?"        | 11/11 con ícono de hechizo, 0 con "?"   |
| 1 (20 min) | Dummies        | Obligatorias 1-8. Focus en un dummy, target en otro. Ciclo: Prowl+Rake al dummy → Cyclone focus → dispel party1 → Bear+Frenzied → salir | Fluye sin mirar barras                  |
| 2 (20 min) | Dummies        | Agregar 9-11. Practicar "juke + Shadowmeld": empezar cast, cortarlo con Meld                                                            | Meld corta el cast el 100% de las veces |
| 3          | Skirmish/duelo | Todo junto con presión real                                                                                                             | 0 clicks de mouse en habilidades        |


Al completar las 4 sesiones: actualizar `02-configuracion/macros_y_ui.md` → **Fase 0.3 cerrada**.

## Reglas simplificadas (cliente esES)

1. **Comandos en inglés, hechizos en español.** `/cast` nunca se traduce; `Ciclón` siempre.
2. **Shift+clic sobre el hechizo, nunca tecleo** — te inmuniza contra el fallo de acentos del cliente español.
3. **Ícono "?" = macro muerta.** Revísalo en cada macro que crees, antes de salir del editor.
4. **Tras cada parche, re-verifica las macros:** los reworks renombran hechizos y la macro muere en silencio (protocolo en `01-plan/guia_revalidacion_s2.md`).
5. **`/use 14` (trinket) es inmune al idioma** — no lleva nombre de hechizo. Por eso es la macro más robusta del set.
6. **Para leer guías (Murlok, Icy Veins, Skill Capped), usa el inglés.** El glosario de arriba es tu puente.