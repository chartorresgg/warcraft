# Tu Kit — Referencia completa de Resto Druid (Midnight S2, 12.1)

> Creado 2026-09-12 porque el proyecto asumía que ya conocías tu clase. **Este archivo explica QUÉ hace cada cosa; los demás explican CUÁNDO usarla.**
> Nombres en inglés (guías) con español entre paréntesis (tu cliente esES).
> ⚠️ **El tooltip in-game gana siempre.** Midnight rediseñó parte del kit y algunas habilidades pasaron a pasivas.

---

## 1. Cómo funciona un Resto Druid (la idea en 60 segundos)

No eres un healer de reacción. **Eres un healer de siembra.**

Tu sanación viene sobre todo de **HoTs** (Heal over Time): hechizos que no curan al instante, sino poco a poco durante segundos. Los pones **antes** de que llegue el daño, y cuando llega, tu equipo ya se está curando solo.

Eso tiene una consecuencia que define todo tu juego:

> **Si esperas a ver la barra de vida bajar, llegas tarde.** Tu trabajo ocurre 5 segundos antes del daño, no durante.

Y el parche de septiembre de 2026 reforzó esto: nerfearon Swiftmend (−20%) y Regrowth (−20%), que son tus curas de reacción, con la intención declarada de que Resto **no dependa de rellenar vida a posteriori**.

---

## 2. Tus HoTs — el motor

| Hechizo | Qué hace | Detalle que importa |
|---|---|---|
| **Rejuvenation** (Rejuvenecimiento) | HoT básico, instantáneo, barato | Tu hechizo más usado. Va **ancho**: en todos los que vayan a recibir daño. Alimenta *Abundance* (con 5+ activos, tu Regrowth gana 50% crítico y cuesta 50% menos) |
| **Lifebloom** (Flor de vida) | HoT sobre 1 objetivo. Con *Everbloom* stackea hasta 3 veces y alcanza a 2 aliados cercanos | **Tu mayor fuente de sanación single-target.** Regla: **nunca se cae** de quien recibe daño. En tu build, además, tu Floración lo sigue |
| **Wild Growth** (Crecimiento salvaje) | HoT de área: cura a varios aliados cerca del objetivo | Instantáneo gracias a *Early Spring*. **Gatilla Grove Guardians.** Es tu hechizo más caro (+15% de maná en 12.1) pero cura 20% más |
| **Regrowth** (Recrecimiento) | Cura directa + un HoT corto. **Casteado** (kickeable) | Caro sin proc. **Con proc de Clearcasting es gratis** — ésa es tu regla de maná |

**El orden mental:** Lifebloom siempre puesto → Rejuvenation ancho → Wild Growth cuando hay daño de área → Regrowth solo con proc.

---

## 3. Tus curas de reacción

| Hechizo | Qué hace | Detalle |
|---|---|---|
| **Swiftmend** (Alivio presto) | Cura instantánea fuerte. **Consume un HoT del objetivo** | ⚠️ **−20% en PvP desde el 1 sep.** Necesita un HoT activo: si llegas sin haber sembrado, no tienes Swiftmend. Gatilla Grove Guardians |
| **Nature's Swiftness** (Presteza de la Naturaleza) | Tu próximo hechizo casteado se vuelve **instantáneo** | **Una sola carga.** Doble uso: Regrowth de emergencia o Cyclone imposible de kickear. **La regla dura del proyecto: si un aliado muere con NS disponible, el error fue tuyo** |
| **Tranquility** (Tranquilidad) | Canalización que cura mucho a todo el equipo | En 12.1 además genera raíces protectoras. Te deja quieto: úsalo con LoS o cuando nadie te presione |
| **Incarnation: Tree of Life** (Encarnación) | Tu CD mayor: te transforma y amplifica el kit | Se tradea **contra los cooldowns ofensivos enemigos**, no contra barras de vida bajas. Duración acortada en PvP desde septiembre |

---

## 4. Tus defensivos — el orden importa

Esta es la escalera. Saltarse peldaños es gastar de más.

| # | Capa | Qué hace |
|---|---|---|
| 1 | **Posicionamiento / pilar** | Gratis. Si puedes romper línea de visión, no gastes nada |
| 2 | **Barkskin** (Piel de corteza) | −30% daño recibido. Usable en CC y transformado. **Úsalo temprano, no lo guardes** |
| 3 | **Bear Form + Frenzied Regeneration** (Forma de oso + Regeneración frenética) | Más vida y armadura + autocuración. Entrar en oso no es perder: es comprar tiempo |
| 4 | **Ironbark** (Corteza de hierro) | Tu único **externo**: reduce daño a un ALIADO. Preventivo, no al 20% de vida |
| 5 | **Trinket** | Rompe CC. **Solo con las 3 condiciones** |
| — | **Shadowmeld** (Fusión de las sombras) | Racial de Night Elf. Rompe targeting y anula casts dirigidos a ti. Con `/stopcasting` corta tu propio cast |

---

## 5. Tu CC — a qué categoría de DR pertenece cada uno

| Hechizo | Categoría DR | Qué hace |
|---|---|---|
| **Cyclone** (Ciclón) | **Disorient** | 6 seg: no actúa, **no recibe daño NI sanación**. Casteado (kickeable) |
| **Rake desde Prowl** (Arañazo) | **Stun** | Aturde al abrir desde sigilo. Requiere estar fuera de combate |
| **Maim** (Amputar) | **Stun** | Aturde 1-5 seg según puntos de combo. Requiere estar en forma felina y haber generado combos |
| **Entangling Roots** (Raíces enredaderas) | **Root** | Inmoviliza. No impide castear |
| **Ursol's Vortex** (Vórtice de Ursol) | **Root** | Zona que arrastra de vuelta a quien intenta salir |
| **Incapacitating Roar** (Rugido incapacitante) | **Incapacitate** | AoE de 3 seg alrededor de ti. **Se rompe con daño** |
| **Typhoon** (Tifón) | Desplazamiento | Empuja y ralentiza (30% desde 12.1) |

> **Detalle crítico de Cyclone:** bloquea *toda* sanación entrante. Por eso sirve en ofensiva (el healer enemigo no cura) y en defensiva (el DPS con cooldowns no hace nada durante 6 segundos).

---

## 6. Movilidad y utilidad

| Hechizo | Uso |
|---|---|
| **Wild Charge** (Carga salvaje) | Según la forma: vuela hacia un aliado (normal), embiste (oso), salta detrás (felina). Tu escape del tren melee |
| **Stampeding Roar** (Rugido de estampida) | Velocidad de área para ti y aliados. **Infravalorado en arena, decisivo en Blitz** |
| **Innervate** (Estimular) | Regenera **20% de tu maná máximo** en 8 seg (PvP). Úsalo al **50-60% de maná** |
| **Nature's Cure** (Cura de la naturaleza) | Tu dispel: quita magia, maldición y veneno. Instantáneo |

---

## 7. Lo que es PASIVO (no busques el botón)

Midnight convirtió varias cosas en pasivas. Esto causó errores reales en este proyecto:

| Talento | Cómo funciona ahora |
|---|---|
| **Grove Guardians** (Fuerza de la Naturaleza) | Los treants salen **solos** al castear **Swiftmend** o **Wild Growth**. No hay botón |
| **Efflorescence** (Floración) | **En tu build** (talento *Lifetreading*) se coloca sola bajo tu objetivo de Lifebloom. Lo que controlas es **en quién pones Lifebloom** |
| **Flourish** | Pasivo: procea al castear Tranquility |
| **Omen of Clarity** (Augurio de claridad) | Pasivo: da procs de *Clearcasting* que hacen tu Regrowth gratis |
| **Everbloom** (Apex) | Pasivo: hace que tu Lifebloom stackee hasta 3 |
| **Abundance** | Pasivo: con 5+ Rejuvenations activos, Regrowth gana 50% crítico y −50% de coste |

---

## 8. Tu prioridad de casteo, momento a momento

### Cuando no pasa nada (el 70% de la partida)

```
1. ¿Lifebloom está activo en quien recibe daño?     → si no, ponlo YA
2. ¿Rejuvenation en los que van a recibir daño?     → siémbralo
3. ¿Tengo proc de Clearcasting?                     → Regrowth gratis
4. ¿Estoy fuera de combate junto a un pilar?        → bebe
```

### Cuando entra daño

```
1. Wild Growth (instantáneo, gatilla treants)
2. Swiftmend sobre alguien que YA tenga HoT
3. Regrowth con proc
4. Ironbark si el go es sobre un aliado concreto
```

### Cuando alguien muere en 3 segundos

```
1. Nature's Swiftness + Regrowth   ← el botón que más vidas salva
2. Swiftmend si hay HoT activo
3. Ironbark
4. Incarnation si todo el equipo está bajo presión
```

### Cuando vienen a por TI

```
1. Pilar / LoS         (gratis)
2. Barkskin            (temprano)
3. Bear + Frenzied
4. Trinket             (solo con las 3 condiciones)
```

---

## 9. Las 10 reglas de tu clase

1. **Siembra antes del daño.** Si reaccionas, llegas tarde.
2. **Lifebloom nunca se cae** de quien recibe daño.
3. **Rejuvenation ancho** — alimenta Abundance y habilita Swiftmend.
4. **Regrowth solo con proc de Clearcasting.** Sin proc es maná quemado.
5. **Wild Growth y Swiftmend gatillan treants.** Son sanación gratis.
6. **Si alguien muere con NS disponible, el error fue tuyo.**
7. **Barkskin temprano, no guardado.** Su CD vuelve; tu vida no.
8. **Cyclone bloquea toda sanación** — ofensivo y defensivo a la vez.
9. **Innervate al 50-60% de maná.** Ni al 90% ni al 20%.
10. **Entrar en Bear no es perder** — es comprar tiempo para que tus HoTs te suban.
