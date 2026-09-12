# Macros, UI y Keybinds — Estado Actual

> Última actualización: **2026-09-11** (sesión de configuración de Fase 0.2 completada)
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

### Macro: [nombre]
```
[COMPLETAR — código de la macro]
```
**Propósito:** [COMPLETAR]

### Macros que sé que me faltan

- [ ] Cyclone @focus / @arena1-2-3 (Ciclón)
- [ ] ~~Bash @focus~~ → **Resto NO tiene Mighty Bash en Midnight.** Tu stun es Prowl+Rake fuera de combate (Acechar + Arañazo) y Maim en combate (Destripar)
- [ ] Ironbark @party1 / @party2 (Corteza de hierro)

> ⚠️ **Tu cliente está en español:** las 11 macros del proyecto ya están traducidas en `02-configuracion/macros_resto_druid.md`. Escritas en inglés NO funcionan — se crean sin error y no hacen nada. Usa siempre **Shift+clic** sobre el hechizo para que el juego escriba el nombre exacto.

## Keybinds

- **Esquema general:** Todo clickeado en las barras de acción. Curas en los slots 1-5 de la barra principal; defensivos en la barra 2, justo encima de los hechizos de la principal.
- **Scroll Mouse:** Scroll abajo: Disipar efectos (Nature's Cure)
- **Movimiento:** W adelante, S atrás, **Q/E strafe**, **A/D giran el personaje** (keyboard turning — ⚠️ a eliminar, ver plan de migración)
- **¿Clicker o keybinder?:** Clicker, en proceso de migración a keybinds (declarado 2026-07-12). Prioridad de migración: habilidades de REACCIÓN primero (trinket, dispel, Bear+Frenzied, Barkskin, Ironbark) — las planificadas pueden esperar.
- **Teclas incómodas que evito usar en momentos de presión:** Sin identificar aún. Regla de detección durante los drills: si bajo presión dudas qué tecla es, el bind está mal ubicado — anotarla aquí y reubicar.

## Plan de migración clicker → keybinds (incremental, un paso por sesión de dummies)

> Adaptado a tu esquema real: strafe en Q/E se CONSERVA (hábito de años). Lo que se elimina es el giro con A/D — al girar con el mouse, A y D quedan libres como teclas de habilidad premium, pegadas a tus dedos de movimiento.

0. **Girar con mouse (botón derecho sostenido), no con A/D.** Es el cambio más incómodo y el más importante: el giro con teclado tiene velocidad fija y lenta — en arena no llegas a kitear ni a reaccionar a swaps. Practicar en dummies/mundo hasta que sea natural. A/D dejan de girar y quedan libres.
1. **Trinket** → botón lateral trasero del mouse
2. **Cyclone @focus** → botón lateral frontal del mouse
3. **Dispel**: ya vive en scroll abajo — solo cambiar su contenido por la macro H (@mouseover) de `02-configuracion/macros_resto_druid.md`. ✅ *Macro H ya creada y funcionando.*
4. **Bear+Frenzied (pánico)** → F
5. **Barkskin** → D (liberada en el paso 0)
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
- [ ] **Paso 0 de la migración: giro con mouse, liberar A/D** ← 🔴 **BLOQUEA TODO LO DEMÁS. Es lo único que queda de Fase 0**
- [ ] Migrar habilidades de reacción a teclas (pasos 1-6 del plan de arriba)
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
