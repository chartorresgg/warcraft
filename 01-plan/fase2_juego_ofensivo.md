# Fase 2 — Juego Ofensivo a Profundidad (Semanas 6-9)

> Verificado: 2026-07-12 contra Icy Veins PvP S1 (Mysticall), Skill Capped, Maxroll (sistema de DR) y datos de Murlok.io.
> ✅ **Actualizado 2026-09-11 a parche 12.1 / Season 2:** el reset de DR ya es de 20 segundos (confirmado en vivo). El sistema y las categorías se mantienen idénticos.
> **Objetivo de fase:** convertirte de healer reactivo a playmaker. Tu prioridad #1 declarada. Aquí vive la diferencia entre 1750 y 1950.
> **Requisito de entrada:** métricas de Fase 1 cumplidas (sanación automática, regla de NS, trades defensivos limpios).

---

## 1. El sistema de DR de Midnight — apréndelo primero

**Regla central:** en PvP, la 1ª aplicación de un CC dura completo, la 2ª dura la mitad, y tras 2 aplicaciones de la misma categoría el objetivo queda **INMUNE** a esa categoría. El DR se resetea **20 segundos** después de que expira la última aplicación (era 16 seg en S1 — cambió con 12.1).

> 💡 **Por qué te conviene el cambio a 20 seg:** con 200 ms de latencia, las ventanas largas te favorecen. Menos goes por partida significa menos momentos donde tu ping decide el resultado, y más peso a la preparación — que es justo donde puedes competir. El DR más lento premia al que planifica sobre el que reacciona.

### Tus CC por categoría de DR

| Tu habilidad (EN → ES) | Categoría | Comparte DR con (ejemplos enemigos) |
|---|---|---|
| **Rake (desde Prowl)** (Arañazo) y **Maim** (**Amputar**) | Stun | Kidney Shot, Storm Bolt, Hammer of Justice, Cheap Shot |
| **Cyclone** (Ciclón) | Disorient | Fear, Dragon's Breath, Blind |
| **Incapacitating Roar** (Rugido incapacitante) | Incapacitante/Disorient — *verificar tooltip in-game en tu build* | Polymorph, Freezing Trap (históricamente) |
| **Entangling Roots / Mass Entanglement / Ursol's Vortex** (Raíces enredaderas / Enredo masivo / Vórtice de Ursol) | Root | Frost Nova, raíces de Hunter |
| **Typhoon** (Tifón) | Desplazamiento | Knockbacks (categoría propia) |

### Las 4 consecuencias prácticas

1. **Cadenas cross-categoría, nunca intra-categoría:** Rake (stun) → Cyclone (disorient) = 4-5 seg + 6 seg completos, porque no comparten DR. Cyclone → Cyclone = 6 + 3 seg y el objetivo queda inmune a disorients. Tu cadena máxima teórica sobre el healer: stun → disorient → root, tres categorías, ~12+ seg de control.
2. **Tu Cyclone comparte DR con el Fear del Warlock/Priest y el Dragon's Breath del Mage.** Si tu DPS acaba de fearear al healer, tu Cyclone encima dura la mitad — y el segundo lo inmuniza. ESTO es lo que hay que cantear en Discord ("healer con DR de disorient") y la causa #1 de Cyclones desperdiciados en equipos descoordinados.
3. **El reloj de 20 seg es tu metrónomo:** tras un intercambio de CC, cuenta ~20 seg desde que expiró para que el DR limpie. Los goes se espacian a ese ritmo — **cuatro segundos más que en S1**, lo que significa ventanas más largas entre setups y más castigo por gastar un CC de más. sArena muestra los DR junto a las barras — úsalo hasta que el conteo sea instinto.
4. **Cada CC responde una pregunta antes de salir:** "¿esto abre un kill o anula un go?" Si la respuesta es "solo molesta", te estás gastando la inmunidad que tu equipo necesitaba en la ventana real.

## 2. Cyclone — el árbol de decisión completo

### Los 4 usos (de Icy Veins, en orden de frecuencia)

| Uso | Situación | Objetivo | Qué logra |
|---|---|---|---|
| **Ofensivo estándar** | Tus DPS abren presión | Healer enemigo (tras Rake/Maim) | 6 seg sin sanar = presión gratis; fuerza su trinket para que el PRÓXIMO setup mate |
| **Negar sanación al kill target** | Tu equipo se queda sin daño y el objetivo está bajo | El propio kill target con poca vida | Cyclone bloquea TODA sanación entrante: el target baja de vida "congelado" mientras tu equipo recupera CDs. Uno de los mejores usos según la fuente |
| **Defensivo** | Go enemigo con CDs ofensivos | El DPS enemigo con CDs activos | 6 seg de su ventana ofensiva evaporados sin gastar defensivos |
| **De asfixia** | Guerra de maná ganada | Healer enemigo repetido (respetando DR) | Cada Cyclone le quema tiempo y maná de recuperación: acelera su OOM |

### ¿Cuándo es seguro hardcastear? (checklist de 1 segundo)

- ✅ El kick del melee que te presiona está en CD (MiniAuras/OmniBar te lo muestra)
- ✅ Estás fuera de línea de visión del caster con interrupt
- ✅ O tienes NS disponible (Call of Ohn'ahra = instantáneo, incastigable)
- ❌ Kick enemigo disponible + estás visible = NO hardcastees. Con tus 200 ms el enemigo ve tu cast tarde pero tú ves su kick MÁS tarde: pierdes ese duelo de reflejos siempre. Muévete de LoS o usa NS.

### La regla del trinket enemigo

El propósito del primer Cyclone al healer casi nunca es matar en ese go: es **forzar su trinket**. Cantéalo SIEMPRE ("healer trinketeó") y a partir de ahí el próximo stun+Cyclone sobre él es ventana de kill real. Inversa: si su trinket está disponible, tu equipo no debe quemar todos los CDs en el primer go.

## 3. Fake casting con 200 ms de latencia

### La teoría adaptada a tu ping

El fake cast estándar: empiezas un cast visible, lo cortas antes de completarlo, el enemigo kickea al aire, y ahora tienes ~15+ seg (CD de su kick) de casts libres. Con 192-201 ms hay una asimetría que debes internalizar: **el enemigo reacciona a información tuya vieja (~0.2 seg), y tú ves sus reacciones tarde.** Traducción operativa:

| Ajuste | Detalle |
|---|---|
| Corta ANTES de tu instinto | Tu barra local va adelantada respecto a lo que el enemigo ve. Si esperas a "ver venir" el kick, ya te llegó. Fakea por ritmo (cortar a ~40-60% del cast), no por reacción |
| Fakea con hechizos baratos | Regrowth es tu señuelo natural: barato de cortar, creíble como amenaza. Nunca fakees con el Cyclone que sí necesitas |
| Usa el indicador de precognition | MiniAuras incluye alerta de kick jukeado: cuando el enemigo kickea al aire, te avisa → esa es tu ventana dorada de hardcast |
| Cuenta kicks en voz alta | "Kick del Warrior usado, 15 seg" — literal, hablando solo. Construye el hábito de canteo para Fase 3 y consolida el tracking mental |

### El drill (sesiones de Shuffle, foco único)

Meta por ronda: sacar **2 kicks enemigos con fakes** sin ser interrumpido en un cast real. Anota por ronda: kicks jukeados / kicks comidos. La proporción debe invertirse a lo largo de la fase (de 0/3 a 2/1).

## 4. Cadenas ofensivas completas

### Cadena A — Opener desde sigilo (puertas o transición fuera de combate)

```
Prowl → Rake al healer enemigo (stun, categoría stun)
→ Cyclone encima (disorient, sin DR compartido)
→ resultado: healer fuera 10-11 seg mientras tus DPS abren
→ vuelta a formas de sanación ANTES de que el daño llegue a tu equipo
```

### Cadena B — Go en combate (la de Forest Guardian)

```
Tus DPS anuncian go (3-5 seg antes)
→ tú pre-cargas: HoTs full en tu equipo, posición cerca del healer enemigo
→ Cat Form: Rake + Shred generan combos (Forest Guardian sostiene tus HoTs)
→ Maim al healer (stun 3-5 seg según combos)
→ Cyclone encima o Roots al peel melee
→ salir de Cat, retomar sanación
```
**Regla de seguridad de la Cadena B:** solo entras a Cat con (a) HoTs completos en los 3, (b) sin go enemigo en curso, (c) NS disponible como airbag. Si falta una, tu contribución al go es Cyclone @focus a distancia y nada más.

### Cadena C — Anti-go (defensiva ofensiva)

```
Detectas CDs ofensivos enemigos (MiniAuras alerta)
→ Ironbark al objetivo + Barkskin si es sobre ti
→ Cyclone al DPS enemigo con CDs (su ventana muere)
→ o Roots al melee (categoría root, barata en DR)
→ Typhoon si necesitas separación física
```

## 5. Posicionamiento anti-CC (tu error recurrente declarado)

### El diagnóstico raíz

Los CC que comes casi nunca son "reflejos lentos" — son **geometría mala 3 segundos antes**. La causa habitual: pararse en la línea recta entre el CCer enemigo y tu equipo (la "autopista"), donde el Poly/Fear te alcanza sin que el enemigo se mueva.

### Las reglas geométricas

| Regla | Detalle |
|---|---|
| **Triángulo, no línea** | Tú en un vértice, tu equipo en otro, fuera de la línea de visión natural del CCer. Que ciclonearte/polymorphearte le exija CAMINAR — cada metro que camina es tiempo de reacción tuyo |
| **Pilar a ≤5 seg, siempre** | Y úsalo PREVENTIVAMENTE: cuando el caster enemigo te mira y no tienes trinket, ya deberías estar rotando al pilar |
| **Max range como hábitat** | Tu curación alcanza 40 yardas; el CC de la mayoría, 30 o menos. Vivir en esa franja de 10 yardas te hace inciclonable |
| **Espalda protegida vs stealth** | Contra Rogue: transiciones con espalda a pilar/pared; el opener por la espalda es su plan A |
| **Muévete tras cada cast** | El hábito de rating alto: cast → paso lateral → cast. Un healer estático es un objetivo de práctica |
| **Tu latencia premia la anticipación** | Con 200 ms, esquivar por reacción es imposible: esquiva por posición. Si el CC nunca tiene ángulo, tu ping no importa |

### El drill de VOD (arranca en esta fase)

Por cada CC completo que comiste en la sesión, pausa el VOD 3 segundos ANTES del cast y pregunta: "¿qué me llevó a estar visible/en rango en ese instante?" La respuesta casi siempre es una decisión de movimiento previa, no el cast en sí. Anota el patrón en el registro.

## 6. Proto-comunicación (puente a Fase 3)

Aunque sigas en Shuffle sin voz, entrena el canteo hablando solo (en serio — funciona):

- "Kick del [X] usado" · "Healer trinketeó" · "Healer con DR de disorient" · "Voy Cyclone en 3"

Cuando llegues a equipos con Discord (Fase 3), estas frases ya saldrán solas. El canteo no se improvisa bajo presión: se automatiza antes.

## 7. Plan de entrenamiento — 4 semanas (8 h/semana)

| Semana | Sesión A (foco único) | Sesión B (foco único) | Drill 30 min |
|---|---|---|---|
| **6** | Solo lectura de DR: cantear en voz alta el estado de DR del healer enemigo en cada go | Solo Cyclone ofensivo estándar (uso 1): 3+ útiles por ronda, 0 en DR | Cadena A en dummies/duelos: Prowl→Rake→Cyclone x10 |
| **7** | Solo fake cast: 2 kicks jukeados por ronda | Solo posicionamiento: ≤1 CC completo comido por ronda | Cadena B en duelos: entrada/salida de Cat con checklist de seguridad |
| **8** | Solo Cyclones defensivos y de negación (usos 2-3) | Integración ofensiva: cadenas completas en Shuffle | VOD: drill de "3 segundos antes" con 2 partidas |
| **9** | Examen: sesión sin foco, todas las métricas a la vez | Examen 2 + registro | Repaso del punto más débil |

## 8. Métricas de salida de fase

- ✅ Puedes decir el estado de DR del healer enemigo en cualquier momento de cualquier ronda
- ✅ 3+ Cyclones que habilitaron presión real por ronda (promedio), 0 desperdiciados en DR
- ✅ 2+ kicks enemigos jukeados por ronda; ≤1 interrupción sufrida por ronda
- ✅ ≤1 CC completo comido por ronda sin trinket forzado
- ✅ Cadena A ejecutada en el 80%+ de las aperturas donde hubo ventana
- ✅ Rating de Shuffle 1850+ (desde 1784)

## 9. Reglas simplificadas

1. **Cadenas cross-categoría:** stun → disorient → root. Nunca dos de la misma.
2. **Tu Cyclone (Ciclón) comparte DR con Fear y Dragon's Breath** — coordina o desperdicia.
3. **2 aplicaciones = inmune. 20 seg de reset.** Ese es el metrónomo de los goes.
4. **Primer Cyclone al healer = forzar trinket. Segundo setup = kill.**
5. **Kick enemigo disponible + tú visible = no hardcastees.** NS o reposición.
6. **Fakea por ritmo, no por reacción** — tus 200 ms pierden todos los duelos de reflejos.
7. **Los CC que comes se deciden 3 segundos antes** — geometría, no reflejos.
8. **A Cat Form solo con HoTs full, sin go enemigo, y NS de airbag.**
9. **Cantea en voz alta aunque juegues solo** — estás entrenando a tu yo de Fase 3.
10. **Cada CC responde: ¿abre kill o anula go?** Si no, no se lanza.
