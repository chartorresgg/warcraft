# Glosario de Conceptos — PvP desde cero

> Creado 2026-09-11. **Este archivo existe porque el resto del proyecto asumía conceptos que nunca explicó.** Si algún término de los otros documentos no te suena, búscalo aquí primero.
> Formato: inglés (el de las guías) con el español entre paréntesis (el de tu cliente).
> Instrucción para Claude: cuando uses un concepto que no esté aquí y sea la primera vez que aparece en el proyecto, explícalo en una línea y añádelo a este archivo.

---

## 1. DR — Diminishing Returns (reducción por repetición)

**La regla que impide que te encadenen control infinito.** Sin ella, dos enemigos podrían turnarse stuns y no volverías a jugar nunca.

Cada efecto de control (CC) pertenece a una **categoría**. Dentro de la misma categoría, sobre el mismo objetivo:

| Aplicación | Duración |
|---|---|
| 1ª | **Completa** — Cyclone dura sus 6 segundos |
| 2ª | **La mitad** — 3 segundos |
| 3ª | **Inmune** — no pasa absolutamente nada |

El contador se reinicia **20 segundos** después de que expira la última aplicación (era 16 seg en S1; cambió con 12.1).

### El detalle que lo hace importante

**La reducción es por categoría, no por hechizo — y las categorías se comparten entre clases distintas.**

Tu **Cyclone (Ciclón)** está en la categoría **Disorient**, junto con el **Fear** del Warlock/Priest, el **Dragon's Breath** del Mage y el **Blind** del Rogue.

Consecuencia: si tu compañero acaba de fearear al healer enemigo y tú le lanzas Cyclone encima, **tu Cyclone dura 3 segundos en vez de 6**. Un tercer disorient no hace nada.

### Tus categorías

| Tus habilidades | Categoría |
|---|---|
| Rake desde Prowl (Arañazo), Maim (Destripar) | **Stun** |
| Cyclone (Ciclón) | **Disorient** |
| Entangling Roots (Raíces enredaderas), Ursol's Vortex (Vórtice de Ursol) | **Root** |
| Incapacitating Roar (Rugido incapacitante) | **Incapacitate** |

Como son categorías **distintas**, no se reducen entre sí. Por eso puedes encadenar:

```
Rake (stun, 4 seg) → Cyclone (disorient, 6 seg completos) → Roots
= ~12 segundos de control, todo a duración máxima
```

**La regla inversa:** nunca dos de la misma categoría seguidas. Cyclone → Cyclone son 6 + 3 seg y luego inmunidad.

### Cómo se ve en pantalla

En los marcos de arena (sArena), **a la izquierda de la barra de vida**. Aparece un iconito solo **cuando alguien ya comió un CC**, con borde de color:

- 🟢 **Verde** — categoría limpia, el siguiente CC dura completo
- 🟡 **Amarillo** — ya comió uno, el siguiente dura la mitad
- 🔴 **Rojo** — inmune, no lances nada de esa categoría

**En una frase:** DR es por qué cada Cyclone cuenta. Antes de lanzarlo: *¿esto abre un kill, o solo gasta el DR que mi equipo necesitaba?*

---

## 2. CC — Crowd Control (control de masas)

Cualquier efecto que impide al enemigo jugar su personaje. No todos son iguales:

| Tipo | Qué hace | Se rompe con daño | Ejemplos tuyos |
|---|---|---|---|
| **Stun** (aturdimiento) | No puede hacer nada | No | Rake desde Prowl, Maim |
| **Disorient** (desorientar) | No actúa, y **no recibe daño ni sanación** | Sí | Cyclone |
| **Incapacitate** (incapacitar) | No puede actuar | Sí | Incapacitating Roar |
| **Root** (raíces) | No se mueve, pero **sí castea y pega** | No (normalmente) | Entangling Roots |
| **Silence** (silencio) | No castea, pero se mueve | No | *(no tienes)* |
| **Slow** (ralentizar) | Camina más lento | No | Typhoon |

**Lo crítico de Cyclone:** bloquea *toda* sanación entrante. Por eso sirve tanto en ofensiva (el healer enemigo no cura) como en defensiva (el DPS con cooldowns no hace nada durante 6 seg).

---

## 3. Vocabulario de arena

| Término | Qué significa |
|---|---|
| **Go** | El momento en que tu equipo abre cooldowns para intentar matar. "Voy go en 3" = prepárate |
| **Kill window** (ventana de kill) | Los segundos en que el enemigo es matable: su healer en CC, sin trinket, sin defensivos |
| **Swap** | Cambiar de objetivo de golpe. "Swap al healer" |
| **Peel** | Quitarle presión a un compañero — raíces al melee que lo persigue, knockback, Ironbark |
| **Kite / kitear** | Huir manteniendo distancia mientras el enemigo te persigue |
| **Trinket** | El accesorio PvP que rompe un CC. Uso limitado (CD largo): por eso la regla de las 3 condiciones |
| **Kick / interrupt** | Interrumpir un cast. Bloquea esa escuela de magia unos segundos |
| **Fake cast / juke** | Empezar un cast y cortarlo para que el enemigo gaste su kick al aire |
| **Hardcast** | Castear un hechizo completo, sin instantáneo. Es lo que el enemigo puede kickear |
| **LoS** (Line of Sight, línea de visión) | Si hay un pilar entre tú y el enemigo, no puede castearte. "Romper LoS" = esconderse |
| **Uptime** | El porcentaje de tiempo que un melee está pegado a su objetivo |
| **Ramp** | Preparar HoTs y escudos *antes* de que llegue el daño |
| **OOM** (Out Of Mana) | Sin maná. Perder la guerra de maná es perder la partida |
| **Overheal** | Sanación desperdiciada sobre alguien que ya está al máximo. Maná tirado |
| **Cleave** | Comp de dos DPS que pegan juntos al mismo objetivo. "Melee cleave" = dos cuerpo a cuerpo |
| **Setup** | La secuencia preparada de CC + daño que produce una muerte |
| **Dampening** (atenuación) | Reducción progresiva de toda la sanación según avanza la arena. Por eso las partidas largas siempre terminan |

---

## 4. Tus marcos en pantalla — qué es cada cosa

| Elemento | Dónde | Qué es |
|---|---|---|
| **Marcos de arena** (sArena) | Derecha | Los enemigos: vida, maná, trinket, DR, cast bar |
| **Marcos de banda / raid frames** | Izquierda | Tu grupo. Tus macros `@party1`/`@party2` apuntan aquí |
| **Placas de nombre** (nameplates) | Sobre las cabezas | Barra de vida flotante + cast bar del enemigo + números 1/2/3 |
| **Gestor de tiempos de reutilización** (Cooldown Manager) | Arriba centro | Tus cooldowns |
| **Números 1/2/3** | Sobre los enemigos | A quién apunta cada macro `@arena1/2/3` |

---

## 5. Abreviaturas que verás en las guías

| Sigla | Significa |
|---|---|
| **HoT** | Heal over Time — sanación progresiva (Rejuvenation, Lifebloom) |
| **DoT** | Damage over Time — daño progresivo |
| **CD** | Cooldown, tiempo de reutilización |
| **GCD** | Global Cooldown — el ~1.5 seg entre hechizos |
| **NS** | Nature's Swiftness (Presteza de la Naturaleza) |
| **WG** | Wild Growth (Crecimiento salvaje) |
| **LB** | Lifebloom (Flor de vida) |
| **Rejuv** | Rejuvenation (Rejuvenecimiento) |
| **Bark** | Barkskin (Piel de corteza) — o Ironbark según contexto |
| **MMR** | Matchmaking Rating — tu nivel real oculto, distinto del rating visible |
| **WR** | Win Rate, porcentaje de victorias |
| **TTK** | Time To Kill — lo rápido que muere alguien en el meta actual |
| **R1** | Rank 1, el 0.1% superior del ladder |

---

## 6. Los cuatro conceptos que más te van a servir

1. **DR es el metrónomo.** Cada CC responde: ¿abre un kill o anula un go? Si no hace ninguna, no se lanza.
2. **Cyclone bloquea sanación.** Es tu herramienta ofensiva Y defensiva.
3. **El trinket se gasta una vez.** Las 3 condiciones: CC completo + alguien bajo 60% + cooldowns enemigos activos.
4. **LoS es gratis, los defensivos no.** Un pilar bien usado ahorra un Barkskin.
