# Macros, UI y Keybinds — Estado Actual

> Última actualización: **2026-09-12** (Fase 0 completa: addons, macros, keybinds y migración clicker→keybinder)
> Instrucción para Claude: este archivo refleja mi configuración ACTUAL. Cuando sugieras mejoras, parte de lo que ya tengo (cambios incrementales), no de una configuración ideal desde cero. Si una sección está vacía, propón una base y explica el porqué de cada elección.

## Addons instalados ✅ (2026-09-11)

Instalados vía **Skill Capped UI** (CurseForge), perfiles core aplicados. Verificado en skirmish.

| Addon | Uso | Estado |
|---|---|---|
| **sArena Reloaded** | Marcos de arena enemigos: vida, maná, trinket, DR, cast bar | ✅ Funcionando — DR visible, maná del healer enemigo legible |
| **MiniAuras** ⚠️ | Todo-en-uno de CC/CDs. **OJO: el proyecto lo llamaba "MiniCC" — el addon real se llama MiniAuras** (v5.40.0) | ✅ Funcionando |
| **FrameSort** | Orden fijo de los marcos de grupo | ✅ Corregido 2026-09-11 (ver nota abajo) |
| **BetterBlizzPlates** | Nameplates: números 1/2/3 sobre enemigos, CC, combo points | ✅ Funcionando |
| **BetterBlizzFrames** | Limpieza de marcos nativos + indicadores | ✅ Instalado (v2.0.7b, marcado EARLY BETA) |
| **Details!** | Medidor de daño/sanación | ✅ Funcionando |

### Configuración aplicada y verificada

| Ajuste | Dónde | Valor |
|---|---|---|
| **Orden de marcos en 3v3** | FrameSort → Arena: 3c3 | **Jugador: Abajo · Ordenar: Grupo** ⚠️ *estaba SIN marcar: causaba que el jugador apareciera 2º o 3º aleatoriamente y rompía las macros @party1/@party2* |
| Orden de marcos en 2v2 | FrameSort → Arena: 2c2 | Jugador: Abajo · Ordenar: Grupo |
| Método de ordenación | FrameSort | **Seguro** (sin taint, permite espaciado) |
| Líder automático | FrameSort | Activado (permite reordenar party1/2 en Solo Shuffle) |
| Solapamiento DR/trinket en marcos de grupo | MiniAuras → Auras importantes | Resuelto ajustando Desplazamiento X/Y y tamaño de icono |
| Interrupciones enemigas | MiniAuras → Interr. enemigas | Activado. **Solo aparece DESPUÉS de que un enemigo gasta su kick** (muestra el CD, no el kick en sí) |

### Pendiente de afinar

- [ ] **"Mostrar nombre" en Interr. enemigas** → activar: con 3 enemigos, el icono no dice *quién* gastó el kick
- [ ] **FrameSort → "Banda (campos de batalla)"** está desmarcado: sin orden fijo en Blitz (opcional — en 8v8 las macros @party1/2 cubren poco)
- [ ] Verificar si existe alerta de "kick jukeado" (precognition) en MiniAuras → **Alertas**
- [ ] Minimapa: se decidió NO eliminarlo (útil en Blitz); pendiente reducir tamaño vía Modo de edición si molesta

## Macros actuales
Nota: Actualmente no uso Macros. Valida si me faltan agregar más.
> Pega aquí tus macros tal como las tienes en el juego. Formato sugerido:

> ✅ **Las 17 macros están creadas y probadas.** El código completo, en español y con su estado de implementación, vive en `02-configuracion/macros_resto_druid.md`. No se duplica aquí para que no se desincronicen.

### Macros que sé que me faltan

- [ ] Cyclone @focus / @arena1-2-3 (Ciclón)
- [ ] ~~Bash @focus~~ → **Resto NO tiene Mighty Bash en Midnight.** Tu stun es Prowl+Rake fuera de combate (Acechar + Arañazo) y Maim en combate (Destripar)
- [ ] Ironbark @party1 / @party2 (Corteza de hierro)

> ⚠️ **Tu cliente está en español:** las 11 macros del proyecto ya están traducidas en `02-configuracion/macros_resto_druid.md`. Escritas en inglés NO funcionan — se crean sin error y no hacen nada. Usa siempre **Shift+clic** sobre el hechizo para que el juego escriba el nombre exacto.

## Keybinds

### ✅ Mapa de teclas REAL (implementado y verificado 2026-09-12)

| Tecla | Qué tiene | Estado |
|---|---|---|
| **1 – 5** | Curas base clickeadas (incluye Recrecimiento y Crecimiento salvaje en 4 y 5) | ✅ Se conservan — son las de menor urgencia de reacción |
| **6** | Libre | ⚪ Disponible |
| **Scroll abajo** | Macro H — Dispel @mouseover (Cura de la naturaleza) | ✅ |
| **Shift+Scroll abajo** | Macro #1 — Dispel @party1 | ✅ Respaldo sin cursor (funciona girando con clic derecho) |
| **Ctrl+Scroll abajo** | Macro #2 — Dispel @party2 | ✅ Igual |
| **Mouse lateral frontal** | Macro #3 — Cyclone @focus (Ciclón) | ✅ La macro más usada |
| **Mouse lateral trasero** | Macro #10 — Trinket (`/use 14`) | ✅ Reacción pura |
| **F** | Macro #8 — Bear + Frenzied Regen | ✅ Botón de pánico |
| **Shift+F** | Macro #9 — NS + Cyclone instantáneo | ✅ |
| **D** | Barkskin (Piel de corteza) | ✅ Liberada al desbindear el giro |
| **A / Shift+A** | Macro A — Ironbark @party1/@party2 | ✅ Liberadas al desbindear el giro |
| **Shift+D** | Macro C — Roots @focus (Raíces enredaderas) | ✅ |
| **R** | Macro D — Wild Charge @party1 (Carga salvaje) | ✅ Escape del tren melee |
| **V** | Macro #11 — Shadowmeld (Fusión de las sombras) | ✅ |
| **Ctrl+1 / Ctrl+2 / Ctrl+3** | Macros #4/#5/#6 — Cyclone @arena1/2/3 | ✅ Elegido 2026-09-12. Coincide con los números 1/2/3 que BBP dibuja sobre los enemigos: ves el "2", pulsas Ctrl+2. **Uso puntual (~10%)**, no de reacción — la incomodidad del modificador es aceptable aquí |
| *(sin asignar)* | Macros #7 Prowl+Rake · #7b Amputar | ⏸️ **Fase 2** — no bindear todavía |

- **Esquema anterior (histórico):** todo clickeado en las barras de acción; curas en 1-5, defensivos en barra 2. **Superado el 2026-09-12** para las habilidades de reacción.
- **Movimiento (actualizado 2026-09-12):** W adelante, S atrás, **Q/E strafe**. ✅ **A/D liberadas** — el giro con teclado quedó desbindeado (las 4 entradas: A, D, Flecha izquierda, Flecha derecha). Ahora se gira con **clic derecho sostenido**.
  - **Esquema de mouse en uso:** clic derecho sostenido = girar el personaje · clic izquierdo sostenido = cámara libre (mirar atrás sin girarse) · ambos botones = *mouse running* (caminar + girar con la mano derecha, mano izquierda libre para habilidades) · clic derecho suelto en el suelo = movimiento por clic.
  - **Vel. giro cámara con ratón: 10** (máximo). Si sobregira al practicar, bajar a 7-8.
- **¿Clicker o keybinder?:** Clicker, en proceso de migración a keybinds (declarado 2026-07-12). Prioridad de migración: habilidades de REACCIÓN primero (trinket, dispel, Bear+Frenzied, Barkskin, Ironbark) — las planificadas pueden esperar.
- **Teclas incómodas que evito usar en momentos de presión:** Sin identificar aún. Regla de detección durante los drills: si bajo presión dudas qué tecla es, el bind está mal ubicado — anotarla aquí y reubicar.

## Plan de migración clicker → keybinds (incremental, un paso por sesión de dummies)

> Adaptado a tu esquema real: strafe en Q/E se CONSERVA (hábito de años). Lo que se elimina es el giro con A/D — al girar con el mouse, A y D quedan libres como teclas de habilidad premium, pegadas a tus dedos de movimiento.

0. **Girar con mouse (botón derecho sostenido), no con A/D.** Es el cambio más incómodo y el más importante: el giro con teclado tiene velocidad fija y lenta — en arena no llegas a kitear ni a reaccionar a swaps. Practicar en dummies/mundo hasta que sea natural. A/D dejan de girar y quedan libres.

   > ✅ **Esquema confirmado in-game el 2026-09-12:** A gira a la izquierda, D a la derecha (sobre su eje) · Q/E desplazan de lado sin girar (strafe) · W/S adelante y atrás. El registro del proyecto era correcto.
   >
   > 🔴 **Método elegido: RADICAL** — desbindear las teclas de giro para que la mano no tenga alternativa.
   > **Dónde:** `ESC → Opciones → Controles → Asignación de teclas` (Key Bindings) → sección **Movimiento** (Movement Keys) → busca **"Girar a la izquierda"** (Turn Left) y **"Girar a la derecha"** (Turn Right) → bórralas.
   > ⚠️ **NO toques** "Desplazarse a la izquierda/derecha" (Strafe Left/Right): ésas son tus Q/E y se conservan.
   > Tras desbindear, A y D quedan libres para asignarles Barkskin e Ironbark (pasos 5 y 6).
1. **Trinket** → botón lateral trasero del mouse
2. **Cyclone @focus** → botón lateral frontal del mouse
3. **Dispel**: ya vive en scroll abajo — solo cambiar su contenido por la macro H (@mouseover) de `02-configuracion/macros_resto_druid.md`. ✅ *Macro H ya creada y funcionando.*
4. **Bear+Frenzied (pánico)** → F
5. **Barkskin** (Piel de corteza) → D (liberada en el paso 0)
6. **Ironbark @party1 / @party2** → A / Shift+A (liberadas en el paso 0)
7. Resto del set (Cyclone @arena1-3, Roots, NS+Cyclone, Shadowmeld) → tabla de `02-configuracion/macros_resto_druid.md`, sustituyendo Q/E por A/D

**Regla de salida por paso:** la habilidad migrada sale por tecla sin mirar la barra, 10 veces seguidas, antes de migrar la siguiente. Las curas 1-5 pueden seguir clickeadas hasta el final — son las de menor urgencia de reacción.

## Hardware / periféricos

- **Mouse:** El mouse tiene dos botones laterales.
- **FPS estables en team fights:** [58 fps]
- **Latencia habitual (ms) desde Bogotá:** [Hogar: 192 ms, Mundo: 201 ms]

## Pendientes de configuración

- [x] ~~Instalar stack de addons~~ ✅ **Hecho 2026-09-11** (sArena Reloaded + **MiniAuras** + FrameSort + BBP + BBF + Details)
- [x] ~~Crear las 11 macros obligatorias~~ ✅ **Hecho 2026-09-12** (11/11 + 6 opcionales, todas probadas in-game)
- [x] ~~**Paso 0: desbindear el giro con teclado**~~ ✅ **Hecho 2026-09-12** — las 4 entradas de "Girar a la izquierda/derecha" en Sin asignar; Q/E de strafe intactas
- [ ] **Paso 0b: construir el hábito** — practicar mouse turning en mundo abierto y dummies. *Criterio: giras 180° sin pensarlo y sin buscar el teclado* ← 🔴 **es lo que queda de Fase 0**
- [x] ~~Migrar habilidades de reacción a teclas~~ ✅ **Hecho 2026-09-12** — 10 de 12 binds implementados y verificados (ver mapa arriba)
- [x] ~~Asignar Cyclone @arena1/2/3~~ ✅ **Ctrl+1/2/3** (4/5/6 ocupadas por curas; Shift resultó incómodo)

### Criterio de ubicación de binds (aprendido en la migración)

La tecla se elige por **frecuencia y urgencia**, no por comodidad absoluta:

| Tipo | Dónde va | Ejemplo |
|---|---|---|
| **Reacción pura** (salvas una vida en <1 seg) | Sin modificador, pegado a la mano | Trinket y Cyclone @focus en los laterales del ratón; Bear+Frenzied en F; Barkskin en D |
| **Puntual pero deliberado** (decides con medio segundo de margen) | Con modificador, se acepta la incomodidad | Cyclone @arena1/2/3 en Ctrl+1/2/3 |
| **Planificado** (lo casteas mirando) | Puede seguir clickeado | Curas base en 1-5 |

⚠️ **Distinguir "incómodo de alcanzar" (reubicar) de "poco familiar" (dar 3 sesiones).** Solo lo primero es un problema de bind.
- [ ] **Quitar de la barra cada hechizo suelto cuya macro ya esté bindeada** (si no, la mano sigue yendo al ratón y la migración no ocurre)
- [ ] Anotar teclas incómodas a medida que aparezcan en los drills

## Regla de sustitución (importante al migrar)

Cuando una macro funciona y tiene tecla asignada, **el hechizo suelto que reemplaza se quita de la barra de acción**. Tener las dos versiones significa que bajo presión clicas la equivocada — y la suelta te cambia el target.

| Macro bindeada | Qué quitar de la barra |
|---|---|
| #1, #2, H — Dispel | Cura de la naturaleza suelto |
| **#3 — Cyclone @focus** | **Ciclón suelto** ← el más importante |
| #8 — Bear + Frenzied | Forma de oso **y** Regeneración frenética sueltos |
| #10 — Trinket | *(nada: estaba en la bolsa)* |
| #11 — Shadowmeld | Fusión de las sombras suelto |
| A — Ironbark | Corteza de hierro suelto |

⚠️ **Excepciones — NO quitar:**
- **Nature's Swiftness (Presteza de la Naturaleza)** suelto: las macros #9 y B compiten por él y tiene **una sola carga**. Necesitas poder elegir en el momento si es Cyclone instantáneo o Regrowth de emergencia.
- **Las curas base** (Rejuvenation, Lifebloom, Regrowth, Wild Growth, Swiftmend): se castean mirando y pueden seguir clickeadas hasta el final. Son las de menor urgencia de reacción.
- Las macros **#4/#5/#6 (@arena1/2/3)** no sustituyen a la #3: conviven. La #3 es tu uso del 90%.
