---
name: aprendizaje-de-promociones
description: Cerrar una promoción o actividad comercial convirtiendo su resultado en aprendizaje reutilizable para todo el equipo - resultado contra línea base, explicación de la desviación y recomendación de repetir, ajustar o detener. Usar cuando el usuario cuente cómo le fue a una promoción.
---

# Aprendizaje de promociones

La parte más valiosa de una promoción no es el uplift: es la lección. Este
skill asegura que cada peso invertido deje conocimiento que otra unidad pueda
reutilizar sin pagar la misma matrícula.

## Cuándo se dispara

El usuario cuenta una promoción, feria, combo o actividad ejecutada — con o
sin buenos resultados.

## Procedimiento

1. **Reúne las piezas** (pregunta lo que falte, en una sola tanda):
   - Mecánica y alcance (qué se hizo, en cuántos puntos, fechas).
   - Inversión con moneda.
   - Resultado CONTRA una línea base ("+18% frente a las 4 semanas
     anteriores"), distinguiendo sell-in de sell-out cuando aplique.
   - Qué explicó la desviación (positiva o negativa).
2. **Destila el aprendizaje**: una regla que otro pueda aplicar, no una
   anécdota. Patrón: "el {mecanismo} funciona cuando {condición}; la próxima
   vez {ajuste}". Ejemplos reales del cerebro: "el obsequio al tendero mueve
   más que el descuento al shopper", "la demostradora convierte más que el
   descuento".
3. **Cierra con una recomendación explícita**: repetir, ajustar (con qué
   cambio) o detener.
4. **Registra** con `registrar_promocion` (cliente, unidad, nombre, inversión,
   resultado, aprendizaje).
5. **Cruza con el resto del gremio**: consulta el cerebro por promociones
   similares de otras unidades y señala al usuario si su aprendizaje confirma
   o contradice uno anterior.

## Antipatrón

Evaluar solo por sell-in ("se vendió todo al cliente") sin preguntar si salió
de la góndola — el cerebro registra las dos mitades.
