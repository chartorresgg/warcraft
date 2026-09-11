# Fase 1 — Sanación Bajo Presión a Profundidad (Semanas 3-5)

> Creado 2026-09-11 con datos de parche **12.1 / Season 2**, incluidos los hotfixes de Blizzard del 1 de septiembre de 2026.
> **Objetivo de fase:** que sanar sea automático, para liberar cerebro para el juego ofensivo (Fase 2). No puedes pensar en Cyclone si aún piensas en Lifebloom.
> **Requisito de entrada:** Fase 0 cerrada — addons instalados, 11 macros creadas y verificadas en español, habilidades de reacción migradas a teclas.
> Nombres: inglés (guías) con español entre paréntesis (tu cliente esES).

---

## 0. Lo que cambió en S2 y por qué esta fase importa más que antes

El hotfix del 1 de septiembre reequilibró tu kit en una dirección concreta:

| Cambio | Consecuencia |
|---|---|
| **Swiftmend −20% en PvP** | Tu heal de reacción más fuerte pega menos |
| **Regrowth −20%** | Tu heal duro también |
| **Sanación general −5%** (con +4% general de vuelta) | Margen neto más ajustado |
| **Innervate rediseñado: 20% de maná en 8 seg** | La guerra de maná cambia de reglas |

Blizzard lo dijo explícitamente: quieren *"que Resto no dependa tanto de Swiftmend para rellenar vida"*. **Traducción para ti: el parche castiga al healer reactivo y premia al preventivo.** Esta fase es exactamente ese entrenamiento — pasó de "buena base" a "requisito para no morir".

---

## 1. El motor de sanación — los 3 modos

No existe "una rotación" de healer. Existen tres modos y el error caro es usar el equivocado.

### Modo A — Mantenimiento (el 70% de la partida)

Nadie está en peligro. Tu trabajo es **preparar**, no curar.

```
Lifebloom (Flor de vida) SIEMPRE en quien recibe daño — nunca se cae
→ Rejuvenation (Rejuvenecimiento) rodando en los 3
→ Efflorescence (Floración) donde va a pelear tu equipo
→ Regrowth (Recrecimiento) SOLO con proc de Clearcasting
→ bebe en cada transición de pilar
```

**La regla de maná de S2:** sin proc de Omen of Clarity, Regrowth es caro. Con proc, es gratis. Si te descubres casteando Regrowth sin proc en Modo A, estás quemando la partida a los 3 minutos.

### Modo B — Presión sostenida (alguien está siendo entrenado)

```
Lifebloom en el objetivo entrenado (con Everbloom stackea a 3 — tu mayor output single-target)
→ Rejuvenation + Regrowth con proc
→ Swiftmend cuando el HoT ya está puesto (consume un HoT: necesita HoT previo)
→ Wild Growth (Crecimiento salvaje) instantáneo vía Early Spring = gatilla Grove Guardians
→ Ironbark (Corteza de hierro) preventivo al inicio del go, no al 20% de vida
```

**Tras el nerf de Swiftmend:** llegar a Swiftmend sin HoTs previos ya no salva a nadie. El HoT ANTES del daño es lo que salva; Swiftmend solo cobra lo que ya sembraste.

### Modo C — Emergencia (burst real, alguien muere en 3 segundos)

Orden estricto, sin improvisar:

```
1. Nature's Swiftness (Presteza de la Naturaleza) + Regrowth  ← el botón que más vidas salva
2. Swiftmend si hay HoT activo
3. Ironbark al objetivo
4. Incarnation: Tree of Life si el equipo entero está bajo presión
5. Tranquility si es daño sostenido en área (12.1: ahora da raíces protectoras)
```

> **La regla dura de esta fase:** si un aliado muere con **NS disponible**, el error fue tuyo. Sin excepciones. Es el fallo #1 estadístico de los Resto Druids en Solo Shuffle, y es la métrica de salida más importante de la fase.

---

## 2. Supervivencia — el orden de trade defensivo

Cuando el swap viene hacia ti, las capas van en este orden. Saltarse capas es como gastar el trinket de primero: te quedas sin nada para el momento real.

| # | Capa | Coste | Cuándo |
|---|---|---|---|
| 1 | **Posicionamiento / pilar** | Gratis | Siempre primero. Si puedes romper línea de visión, no gastes nada |
| 2 | **Barkskin** (Piel de corteza) | CD corto | 30% de reducción. Úsalo TEMPRANO en el swap — no lo guardes, el CD vuelve |
| 3 | **Bear Form + Frenzied Regen** (Forma de oso + Regeneración frenética) | Pierdes casting | Cuando Barkskin no basta. Entrar a Bear no es perder: es comprar tiempo para que tus HoTs te suban |
| 4 | **Ironbark** (a ti mismo o al aliado) | CD medio | Si el go es sobre un aliado, va a él |
| 5 | **Trinket** | CD largo | Solo bajo la regla de 3 condiciones ↓ |

### La regla del trinket (tu duda declarada)

Trinketea **solo si se cumplen las tres**:

1. Estás en **CC completo** (no un slow, no un root que puedes shiftear), **Y**
2. Tú o un aliado está **bajo 60% de vida**, **Y**
3. Los **CDs ofensivos enemigos están activos**.

Si falta una, **come el CC**. El trinket gastado temprano es la causa #1 de muertes evitables: el CC que te mata nunca es el primero, es el segundo.

> **Nota de tu latencia:** con 200 ms no puedes trinketear "por reacción" a un stun de 3 segundos — para cuando lo ves y reaccionas, se te fue medio stun. Trinketea por **lectura**: si ves los CDs enemigos abrirse, ya sabes lo que viene.

---

## 3. La guerra de maná en S2 (sección reescrita por el rework de Innervate)

**Innervate (Estimular) es otro hechizo.** En S1 hacía tus hechizos gratis 8 segundos y se alineaba con una ventana de spam. En S2 regenera **20% de tu maná máximo en 8 segundos** en PvP (el tooltip dice 25%; el hotfix del 1 de septiembre lo bajó a 20% solo en combate PvP).

| Antes (S1) | Ahora (S2) |
|---|---|
| Ventana de spam: castea todo lo caro mientras dura | Chupito de maná: es una recarga, no una ventana |
| Se usaba con el ramp ofensivo | Se usa cuando empiezas a perder la guerra de maná |
| Curabas más durante esos 8 seg | Curas igual; simplemente tienes más maná después |

**La regla nueva:** úsalo alrededor del **50-60% de maná**.
- Al 90% desperdicias el grueso de la regeneración (no puedes exceder tu máximo).
- Al 20% ya perdiste — llegas tarde y con el equipo muerto.

**Las tres fuentes de maná que sí controlas:**
1. **Beber en transiciones.** Cada pilar, cada momento fuera de combate. BetterBlizzFrames te avisa cuándo puedes.
2. **Regrowth solo con proc.** Es la mitad de tu gasto evitable.
3. **No spamear Rejuvenation en overheal.** Un Rejuv en alguien al 100% que no va a recibir daño es maná tirado.

---

## 4. Posicionamiento (inicio — se profundiza en Fase 2)

Dos reglas, nada más. El desarrollo completo está en `fase2_juego_ofensivo.md` §5.

- **Regla de max range:** si un melee enemigo puede tocarte sin usar gap closer, estás mal parado.
- **Un pilar siempre a ≤5 segundos de tu posición.** Si no lo tienes, tu siguiente movimiento es hacia él.

---

## 5. Laboratorio — 3 semanas (8 h/semana)

Un foco por sesión. Es entrenamiento de gimnasio, no partido: el rating aquí es termómetro, no objetivo.

| Semana | Sesión A (foco único) | Sesión B (foco único) | Drill 30 min |
|---|---|---|---|
| **3** | Solo HoT upkeep: Lifebloom nunca se cae, Rejuv en los 3 | Solo no morir: capas defensivas en orden, sin trinket prematuro | Dummies: Modo C completo (NS+Regrowth, Swiftmend, Ironbark) x15 |
| **4** | Solo la regla de NS: 0 muertes de aliado con NS disponible | Solo guerra de maná: Innervate al 50-60%, beber en cada transición | Dummies: ciclo de Modo A hasta que salga sin mirar barras |
| **5** | Solo regla de trinket: verificar las 3 condiciones en voz alta antes de usarlo | Examen: sesión sin foco, todas las métricas a la vez | Repaso del punto más débil de las 3 semanas |

**Formato:** 2 sesiones de Solo Shuffle por semana, 6 rondas cada una.

---

## 6. Métricas de salida de fase

- ✅ **0 muertes de aliados con NS disponible** en una sesión completa (la métrica reina)
- ✅ 3 sesiones seguidas de Shuffle **sin morir teniendo Barkskin + Bear disponibles**
- ✅ Lifebloom activo en el objetivo entrenado **>90% del tiempo** de cada ronda
- ✅ Trinket usado **solo bajo la regla de 3 condiciones** (revisar mentalmente post-ronda)
- ✅ Innervate usado en la ventana 50-60% de maná, no antes ni después
- ✅ **Rating de Shuffle estable o subiendo** desde donde estés al empezar la fase

---

## 7. Reglas simplificadas

1. **Lifebloom (Flor de vida) nunca se cae** de quien recibe daño — Everbloom es tu motor de output.
2. **Aliado bajo 50% con burst encima + NS disponible → NS ya.** Sin excepciones.
3. **El HoT antes del daño es lo que salva.** Swiftmend solo cobra lo que ya sembraste — y desde septiembre cobra 20% menos.
4. **Orden defensivo:** pilar → Barkskin → Bear+Frenzied → Ironbark → trinket.
5. **Trinket solo con las 3 condiciones.** Si falta una, come el CC.
6. **Innervate al 50-60% de maná.** Es un chupito, no una ventana de spam.
7. **Regrowth sin proc de Clearcasting es maná quemado.**
8. **Barkskin temprano, no guardado.** Su CD vuelve; tu vida no.
9. **Con 200 ms, trinketea por lectura, no por reacción.** Si ves abrir sus CDs, ya sabes lo que viene.
10. **Este parche castiga al healer reactivo.** Prepara, no apagues incendios.
