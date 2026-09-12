# Guía de Revalidación — protocolo para parches mayores

> Propósito: protocolo paso a paso para actualizar TODO tu setup cuando llega un parche mayor, sin depender de memoria. Escrito el 2026-07-12 con datos del PTR de 12.1.
>
> ## ✅ EJECUTADA el 2026-09-11 para 12.1 / Season 2
>
> El parche salió el **11 de agosto de 2026** y Season 2 arrancó el **18 de agosto**. Esta guía se ejecutó con ~3 semanas de retraso; los resultados están aplicados en `talentos_core.md`, `talentos_flexibles.md`, `fase1_sanacion_bajo_presion.md`, `fase2_juego_ofensivo.md`, `roadmap_fases.md`, `perfil_jugador.md` y `CLAUDE.md`.
>
> **Contraste PTR (julio) vs. realidad (septiembre) — lo que el PTR NO acertó:**
>
> | Predicción del PTR | Qué pasó de verdad |
> |---|---|
> | Innervate: 25% de maná | **20% en PvP** — hotfix del 1 de septiembre |
> | Ancient of Lore cambiaría la tríada de PvP talents | **No entró: 3/50.** La tríada siguió idéntica |
> | *(no previsto)* | **Nerfs del 1 de septiembre:** Swiftmend −20%, Regrowth −20%, sanación general −5%, Incarnation acortado |
> | *(no previsto)* | Ursol's Vortex saltó de 27 a 43/50; Typhoon subió a 41/50 pese al nerf de su slow |
>
> **Lección para la próxima vez:** el PTR acierta en la dirección y falla en los números. Los hotfixes de las 2-3 semanas posteriores al lanzamiento importan tanto como el parche — revisa siempre las notas de hotfix, no solo el changelog del parche.
>
> **Próxima ejecución:** siguiente parche mayor. Todo lo de abajo sigue vigente como protocolo reutilizable.

---

## 1. Cambios conocidos del PTR que te afectan (verificar valores finales al lanzamiento)

| Cambio | Impacto en tu juego | Archivo del proyecto a actualizar |
|---|---|---|
| **DR reset: 16 → 20 seg** | Los goes se espacian más; tu metrónomo mental cambia. Ventanas entre setups más largas | `fase2_juego_ofensivo.md` |
| **Innervate rediseñado:** de "hechizos gratis" a regenerar maná en 8 seg — **20% en PvP** (el tooltip dice 25%; hotfix del 1 sep) | Muere la ventana de spam gratis; nace un "chupito de maná". Ya no se alinea con el ramp — se usa al empezar a perder la guerra de maná | ✅ Aplicado en `fase1_sanacion_bajo_presion.md` §3 |
| **Ancient of Lore regresa como PvP talent** | Posible cambio en tu tríada estándar de PvP talents — verificar en Murlok qué desplaza | `talentos_flexibles.md`, tabla de PvP talents |
| **Genesis rework + Overgrowth y Flash of Clarity nuevos; Nature's Splendor eliminado** | El árbol de Resto cambia de forma: re-importar build completo, no parchear el viejo | `talentos_core.md`, `talentos_flexibles.md` |
| **Wild Growth +20% healing / +15% maná; Lifebloom -20% maná; buffs a Swiftmend; Tranquility gana raíces protectoras; Incarnation castea Regrowth en 3 aliados al activarse** | Tu Modo C de burst-healing probablemente se reordena | `fase1_sanacion_bajo_presion.md` §1 |
| **Typhoon: slow 50% → 30%** | Baja de valor en tus flex de matchup vs casters | `talentos_flexibles.md` |
| **+25% vida y daño enemigo aumentado (tuning global 12.1)** | El ritmo de las partidas cambia: TTK distinto, recalibrar tu instinto de pánico | Mental, no archivo |
| **Indicador nativo de kicks fallados** | Herramienta nueva para tu juego de fake cast — configurarla | `addons_ui_programas.md` |
| **Season 2: reset de rating + gear nuevo** | Rating a 0, iLvl a renovar, tier set nuevo (recuerda: sets al 33% en PvP pero relevantes), dos trinkets PvP siempre | `perfil_jugador.md`, `registro_temporada.md` |

## 2. Protocolo de revalidación — Día 1 del parche (~2 horas, SIN colar puntuado)

| # | Paso | Fuente | Hecho |
|---|---|---|---|
| 1 | Leer el changelog de Resto Druid PvP | Icy Veins (registro de cambios al pie de cada página de la guía de Mysticall) | ☐ |
| 2 | **Actualizar addons** (CurseForge → Update All) y verificar en un skirmish que sArena/MiniAuras/FrameSort sobrevivieron al parche | CurseForge App | ☐ |
| 3 | **Re-verificar TODAS las macros con Shift+clic** — los reworks renombran hechizos y una macro con nombre viejo muere en silencio. Ícono "?" = macro rota | In-game, editor de macros | ☐ |
| 4 | Importar el build nuevo de Skill Capped (botón Copy Import String) — NO parchear el loadout viejo: crear "SC Standard S2" | skill-capped.com → Resto Druid → Talents | ☐ |
| 5 | Configurar el indicador nativo de kicks fallados | Opciones/Edit Mode | ☐ |
| 6 | Sesión de dummies de 30 min: Modo C nuevo, macros verificadas, sensaciones del tuning | In-game | ☐ |

## 3. Protocolo — Semana 1 de Season 2

| # | Paso | Fuente | Hecho |
|---|---|---|---|
| 7 | **Esperar ~5-7 días y contrastar contra el heatmap de Murlok** (los top necesitan días para asentar el meta nuevo; el día 1 el heatmap muestra ruido) | murlok.io/druid/restoration/3v3 | ☐ |
| 8 | Verificar Hero Talent dominante (¿sigue Keeper 48/50?) | Murlok, contador superior | ☐ |
| 9 | Verificar tríada de PvP talents (¿Ancient of Lore desplazó a Forest Guardian o a otro?) | Murlok, sección PvP Talents | ☐ |
| 10 | Gemas/enchants/embellishments nuevos de S2 | Murlok, secciones Gems/Enchantments | ☐ |
| 11 | Revisar comps meta de S2 con Resto Druid (para tu búsqueda de equipo de Fase 3) | Skill Capped comps + datos de ladder | ☐ |
| 12 | **Build de RBG por separado** (tu bracket fuerte se reactiva en S2) | murlok.io/druid/restoration/rbg | ☐ |
| 13 | Inspeccionar a los top de tu server (Fofy, Bntyx u otros que aparezcan en el top 50) | Murlok / in-game | ☐ |
| 14 | Gear: plan de capeo semanal de S2, dos trinkets PvP, tier set nuevo | Icy Veins Gear page | ☐ |
| 15 | Actualizar los archivos del proyecto marcados en la tabla §1 | Este proyecto | ☐ |

## 4. Estrategia de rating para el arranque de S2

| Regla | Razón |
|---|---|
| **Semana 1: no puntuado serio.** Solo Shuffle y skirmish mientras el meta asienta y tu gear sube | El MMR temprano con gear a medias y meta desconocido produce derrotas que no enseñan nada |
| **Semanas 2-3: placement con calma en 3v3/Shuffle** | Tu MMR histórico te reposiciona rápido; no hay premio por correr |
| **El push real empieza con gear competitivo + build validado contra Murlok** (típicamente semana 3-4) | Empujar rating con desventaja de iLvl es entrenar frustración |
| **RBG: solo con comunidad organizada desde el inicio** | A tu nivel (2100+) el random LFG de RBG es lotería; usa las comunidades identificadas en Fase 3 |
| Recordatorio del roadmap: tus récords (1750/2100) se atacan EN S2, con Fases 1-2 completadas | Ese fue siempre el plan — S1 fue laboratorio |

## 5. Qué NO cambia con el parche (tu capital permanente)

Todo lo mecánico sobrevive a cualquier parche: la lógica de categorías de DR y cadenas cross-categoría, el árbol de decisión de Cyclone, el fake casting por ritmo, la geometría de posicionamiento (triángulo, max range, pilar), la regla de NS, el orden de capas defensivas, la regla de trinket de 3 condiciones, el protocolo de comunicación, la revisión de VODs y las reglas anti-tilt. **Los archivos de fases se retocan; no se rehacen.**

## 6. Prompt de revalidación listo para pegar (en un chat nuevo de este proyecto)

```
Estamos en [FECHA]. El parche 12.1 y la Season 2 de Midnight ya están en vivo.
Ejecuta la "Guía de Revalidación S2" del proyecto (guia_revalidacion_s2.md):

1. Busca en la web el estado FINAL de los cambios de Resto Druid PvP en 12.1
   (Icy Veins changelog, Skill Capped) y compáralo con la tabla §1 de la guía:
   señala qué cambió respecto al PTR.
2. Contrasta el build vigente contra el heatmap de murlok.io/druid/restoration/3v3:
   hero talent dominante, tríada de PvP talents (¿entró Ancient of Lore?),
   talentos core 48-50/50 y flex de zona media.
3. Dame la lista de correcciones concretas para actualizar:
   talentos_core.md, talentos_flexibles.md, fase1 (§ maná/Innervate y Modo C)
   y fase2 (§ DR con reset de 20 seg).
4. Verifica gemas/enchants/embellishments y tier set de S2.
5. Dame el build de RBG actualizado desde murlok.io/druid/restoration/rbg.
Recuerda: cliente esES (nombres de macros via Shift+clic), Mighty Bash NO existe
para Resto (stun = Prowl+Rake / Maim), y mis datos de juego están en perfil_jugador.md.
```

## 7. Reglas simplificadas

1. **Día 1: addons, macros (Shift+clic), build importado, dummies. Cero puntuado.**
2. **El heatmap de Murlok necesita ~1 semana para decir la verdad** — no copies el meta del día 1.
3. **Las macros mueren en silencio con los renombres** — ícono "?" es tu alarma.
4. **Innervate es otro hechizo en S2** — reaprender, no asumir.
5. **El metrónomo de DR pasa de 16 a 20 segundos** — goes más espaciados.
6. **Push de rating desde la semana 3-4,** con gear y build validados.
7. **Lo mecánico no caduca:** las Fases 1-2 entrenadas son tu ventaja de arranque en S2.
