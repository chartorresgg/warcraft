# Fase 4 — Mejora Sostenida y Push a Récords (Semana 13 en adelante)

> Creado 2026-09-12.
> **Objetivo:** superar 1750 en 3v3 (meta 1950+) y 2100 en RBG (meta 2200+) con un sistema, no con grinding ciego.
> **Requisito de entrada:** Fases 1-3 cumplidas. Sanación automática, Cyclone con timing, equipo fijo y protocolo de voz.
> A diferencia de las fases anteriores, **ésta no termina**. Es el modo de operación permanente.

---

## 1. La proporción que separa a quien sube de quien se estanca

Con 8 horas semanales:

| | Jugador promedio | Quien sube |
|---|---|---|
| Colas puntuadas | 100% | **75%** (≈6 h) |
| VOD + drills | 0% | **25%** (≈2 h) |

**Jugar más no es entrenar más.** Las partidas te dan repeticiones; los VODs te dicen qué repetir.

---

## 2. Revisión de VODs

### Configuración

- **OBS Studio** con *replay buffer* activo (o la grabación nativa de Windows: `Win+G`)
- Solo partidas puntuadas — las de práctica no se revisan

### Frecuencia

**2 partidas por semana: una derrota cerrada + una victoria.** Más que eso es procrastinación disfrazada de estudio.

> La victoria se revisa por una razón concreta: para saber **qué hiciste bien y por qué funcionó**. Si solo revisas derrotas, aprendes a evitar errores pero no a repetir aciertos.

### Qué buscar — el checklist de 4 preguntas

| Evento | Pregunta |
|---|---|
| **Cada CC que comiste** | ¿Qué me llevó a estar visible/en rango 3 segundos antes? |
| **Cada muerte de aliado** | ¿Tenía NS disponible? ¿Ironbark? → si sí, el error fue mío |
| **Cada Cyclone** | ¿Abrió un kill, anuló un go, o solo gastó DR? |
| **Cada trinket** | ¿Se cumplían las 3 condiciones? |

### El drill de "3 segundos antes"

Por cada CC completo que comiste, **pausa el VOD 3 segundos ANTES del cast** y pregunta qué decisión de movimiento te dejó expuesto.

La respuesta casi nunca es "reaccioné tarde". Casi siempre es **geometría mala tomada antes**. Ése es tu error recurrente declarado, y es el drill que lo ataca directamente.

---

## 3. Gestión mental

| Regla | Detalle |
|---|---|
| **3 derrotas seguidas → parar** | Ya la tienes. Añadido: la revisión post-racha **cuenta como sesión de entrenamiento**, no como tiempo perdido |
| **Las sesiones de foco único son inmunes** | Shuffle con un objetivo concreto es laboratorio. El rating ahí es termómetro, no objetivo |
| **No colar puntuado en días de [COMPLETAR]** | ⚠️ Pendiente de rellenar en `04-seguimiento/registro_temporada.md` — sin esto la regla no opera |
| **Máximo 5-6 h de colas puntuadas por semana** | Las otras 2 h son VOD y drills |

> **La trampa del rating:** después de una racha mala, el impulso es colar más para "recuperar". Eso es exactamente lo que baja el rating. La recuperación se hace revisando, no jugando.

---

## 4. El ciclo semanal

```
Fin de semana (sesiones de juego)
  → registrar cada sesión en registro_temporada.md (2 min)
  → grabar las puntuadas

Entre semana (2 h)
  → revisar 1 derrota cerrada + 1 victoria
  → anotar hallazgos en el registro
  → elegir UN foco para la siguiente sesión

Cada 2-3 semanas
  → análisis de patrones: ¿qué error se repite?
  → ajustar el foco de las sesiones siguientes
```

**El registro es el motor de todo esto.** Sin datos no hay patrones, y sin patrones el VOD solo te dice qué pasó en esa partida concreta.

---

## 5. RBG y Blitz — tu bracket fuerte

Tus fundamentos de 2100 siguen ahí. Lo específico:

| Aspecto | Detalle |
|---|---|
| **Build separado** | Murlok tiene páginas distintas de RBG y Blitz. **Stats invertidos: Versatility > Mastery** |
| **Addons de BG** | BattleGroundEnemies Fixed + Win Conditions + Capping (ya instalados, solo activarlos) |
| **Tu rol** | Healer de flag carrier. Todo el posicionamiento anti-CC de Fase 2 **es supervivencia de FC** |
| **RBG de grupo** | Solo con comunidad organizada. A 2100+ el LFG random es lotería |

> **Hipótesis pendiente de validar:** tu 38% de win rate en Blitz se registró sin herramientas. Tras 3-4 sesiones con la configuración nueva, si ese número sube solo, confirmado. Si no sube, hay conocimiento del formato que atacar — y entonces toca escribir una guía de Blitz específica.

---

## 6. Cuándo revalidar el meta

Ejecuta `01-plan/guia_revalidacion_s2.md` cuando:

- Llegue un **parche mayor** (cambian talentos, builds, DR, tuning)
- Pasen **2-3 semanas tras un parche** (los hotfixes importan tanto como el parche — lección aprendida en septiembre de 2026)
- Empiece una **temporada nueva** (reset de rating, gear nuevo, meta distinto)

---

## 7. Métricas de fase (rolling, no de salida)

- ✅ **2 VODs/semana** revisados con notas escritas
- ✅ **Todas las sesiones registradas** en `registro_temporada.md`
- ✅ Tendencia de rating **positiva en ventanas de 3 semanas** (no día a día)
- ✅ Hitos de la temporada tachándose
- ✅ La proporción 75/25 respetada

---

## 8. Reglas simplificadas

1. **75% jugar, 25% estudiar.** La proporción del jugador promedio es 100/0.
2. **2 VODs por semana: una derrota cerrada y una victoria.** Más es procrastinar.
3. **El drill de "3 segundos antes"** ataca tu error recurrente: los CC se deciden por geometría previa.
4. **Si un aliado murió con NS disponible, el error fue tuyo.** Sin excepciones, en cualquier fase.
5. **Tras 3 derrotas, parar.** Revisar cuenta como entrenar.
6. **Registra cada sesión.** 2 minutos. Sin datos no hay patrones.
7. **La tendencia se mide en semanas, no en partidas.**
8. **Revalida el meta tras cada parche** — y espera a los hotfixes.
