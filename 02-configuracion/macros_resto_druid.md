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
| Maim | **Destripar** | No |
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
| 7   | **Prowl + Rake (tu stun de apertura)** | `#showtooltip Arañazo` `/cast [noform:1] Forma felina` `/cast [nostealth] Acechar` `/cast [stealth] Arañazo` ⚠️ Shift+clic en Arañazo    | Toques sucesivos: Cat Form → Prowl (sigilo) → Rake, que **desde sigilo aturde**. ⚠️ Resto NO tiene Mighty Bash en Midnight — este es tu stun real | Antes de abrir puertas o en transiciones fuera de combate: Prowl → Rake al healer enemigo → Cyclone encima | Es el opener estándar del spec según Icy Veins. Prowl requiere estar fuera de combate; en pelea tu stun es Maim (fila 7b)                                              |
| 7b  | **Maim (stun en combate)** (Destripar) | `#showtooltip` `/cast Destripar`                                                                                                         | Stun en melee que consume puntos de combo (1-5 seg según combos)                                                                                  | En Cat Form pegado al objetivo: Rake/Shred generan combos → Maim aturde                                    | 49/50 de los top lo talentan. *Forest Guardian* (tu PvP talent) existe para esto: agredir en Cat sin que tus HoTs mueran. Jugada de Fase 2+, no la fuerces en semana 1 |
| 8   | **Bear + Frenzied Regen**              | `#showtooltip` `/cast [nostance] Forma de oso` `/cast [form:2] Forma de oso` `/cast [form:3] Forma de oso` `/cast [form:1] Regeneración frenética` ⚠️ Shift+clic | 1er toque = Bear Form (desde cualquier forma); 2do toque = Frenzied Regen                                                                         | El swap viene hacia ti y Barkskin no basta: spamea la tecla                                                | Bajo pánico no hay tiempo de "primero forma, luego heal". Un botón = capa defensiva 2 completa                                                                         |
| 9   | **NS + Cyclone instantáneo**           | `#showtooltip` `/cast Presteza de la Naturaleza` `/cast Ciclón` ⚠️ Shift+clic                                                            | Con *Call of Ohn'ahra*: Cyclone instantáneo, imposible de kickear                                                                                 | Momento clutch: kill window abierto, sin tiempo de hardcast                                                | Con tus 200 ms, el único Cyclone que tu ping no puede arruinar. Variante: última línea `/cast [@focus] Ciclón`                                                         |
| 10  | **Trinket PvP**                        | `#showtooltip` `/use 14`                                                                                                                 | Usa el accesorio del slot 14 (Medallion). Si está arriba, cambia a `/use 13`                                                                      | Solo con la regla de 3 condiciones (CC completo + aliado/tú <60% + CDs enemigos activos)                   | Trinket clickeado desde bolsa = trinket tarde. Tecla dedicada, siempre la misma. **Sin nombre de hechizo = inmune al idioma** |
| 11  | **Shadowmeld instantáneo**             | `#showtooltip` `/stopcasting` `/cast Fusión de las sombras` ⚠️ Shift+clic                                                                | Corta tu cast y te desvanece: pierden target sobre ti; casts dirigidos a ti fallan                                                                | Uso pro: el caster enemigo termina su CC hacia ti → Meld en el último instante → el cast se pierde         | Eres Night Elf: este racial es la razón por la que el 98% de los top lo son (50/50 en el top de 3v3 este parche). Sin macro no corta tu propio cast                    |




## OPCIONALES — agregar en semanas 2-4, en este orden


| #   | Macro                             | Código (⚠️ nombres en ESPAÑOL — cliente esES)                                                                    | Qué hace / Cuándo                                                                                               | Nota                                                                               |
| --- | --------------------------------- | ---------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| A   | **Ironbark @party1 / @party2** (Corteza de hierro) | `#showtooltip` `/cast [@party1] Corteza de hierro` *(duplicar para party2)*                     | Tu externo instantáneo al aliado, al inicio del go enemigo sobre él                                             | Sube a obligatoria en Fase 1. Opcional solo mientras te acostumbras al resto       |
| B   | **NS + Regrowth (pánico)**        | `#showtooltip` `/castsequence reset=3 Presteza de la Naturaleza, Recrecimiento`                                  | 1er toque NS, 2do Regrowth instantáneo (se reinicia a los 3 seg)                                                | ⚠️ Compite por NS con #9. NS es UNA carga: decide en el momento si es heal o CC    |
| C   | **Entangling Roots @focus** (Raíces enredaderas) | `#showtooltip` `/cast [@focus] Raíces enredaderas` ⚠️ Shift+clic                                   | Roots al focus: peel o separar al healer enemigo de su equipo                                                   | Versiones @arena123 si escalas                                                     |
| D   | **Wild Charge @party1 / @party2** (Carga salvaje) | `#showtooltip` `/cast [@party1] Carga salvaje` *(duplicar para party2)*                           | Vuelas hacia tu aliado: escape instantáneo del tren melee                                                       | Salvavidas lejos de pilares                                                        |
| E   | **Efflorescence @cursor** (Floración) | `#showtooltip` `/cast [@cursor] Floración` `/ping` ⚠️ Shift+clic                                             | Suelta la flor donde está el cursor, sin círculo verde, y pinguea al equipo                                     | Ahorra ~0.5 seg por uso, muchas veces por partida                                  |
| F   | **Talento flexible: AoE CC**      | `#showtooltip` `/cast [known:Enredo masivo] Enredo masivo` `/cast [known:Vórtice de Ursol] Vórtice de Ursol` ⚠️ Shift+clic | Usa automáticamente el talento que tengas en esa fila                                              | A prueba de swaps de matchup (Fase 4): cambias talentos sin reorganizar barras. ⚠️ `known:` también necesita el nombre en español |
| G   | **Incapacitating Roar** (Rugido incapacitante) | `#showtooltip` `/cast Rugido incapacitante`                                                         | CC de área de 3 seg (se rompe con daño) — tu incapacitate cuando lo talentas (flex, 34/50 de uso en S2)         | Solo si está en tu build. Coordina en voz antes de usarlo: el daño propio lo rompe |
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