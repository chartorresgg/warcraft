# Macros, UI y Keybinds — Estado Actual

> Última actualización: 2026-07-11
> Instrucción para Claude: este archivo refleja mi configuración ACTUAL. Cuando sugieras mejoras, parte de lo que ya tengo (cambios incrementales), no de una configuración ideal desde cero. Si una sección está vacía, propón una base y explica el porqué de cada elección.

## Addons instalados
Nota: Actualmente no tengo addons instalados. 

| Addon | Uso | ¿Configurado bien? |
|---|---|---|
| [COMPLETAR — ej. OmniBar] | Tracking de CDs enemigos | Sí / No / No sé |
| [COMPLETAR — ej. Gladius / sArena] | Frames de arena | |
| [COMPLETAR — ej. BigDebuffs] | Prioridad de debuffs/CC en frames | |
| [COMPLETAR — ej. WeakAuras] | Alertas personalizadas | |
| [COMPLETAR — ej. OmniCC / TrufiGCD] | | |

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
3. **Dispel**: ya vive en scroll abajo — solo cambiar su contenido por la macro H (@mouseover) de `02-configuracion/macros_resto_druid.md`
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

- [ ] Paso 0 de la migración: giro con mouse, liberar A/D (bloquea todo lo demás)
- [ ] Migrar habilidades de reacción a teclas (pasos 1-6 del plan de arriba)
- [ ] Instalar stack de addons (sArena Reloaded + MiniCC + FrameSort) — ver `02-configuracion/addons_ui_programas.md`
- [ ] Crear las 11 macros obligatorias — ver `02-configuracion/macros_resto_druid.md`
- [ ] Anotar teclas incómodas a medida que aparezcan en los drills
