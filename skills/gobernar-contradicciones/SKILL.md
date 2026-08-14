---
name: gobernar-contradicciones
description: Gobernar el conocimiento compartido cuando dos registros dicen cosas opuestas sobre el mismo cliente - detectar el conflicto con sus fuentes, llevarlo a la mesa redonda del equipo y registrar el veredicto como acta. Usar cuando aparezcan versiones contradictorias o el usuario pregunte "cómo está" un cliente y las señales choquen.
---

# Gobernar contradicciones

Un cerebro compartido sin gobierno es un rumor con memoria perfecta. Este
skill convierte el conflicto en el momento más valioso del CRM: detectar,
arbitrar en equipo y dejar acta.

## Cuándo se dispara

Dos registros del CRM se contradicen (un cliente "quemado" para una unidad y
"perfecto" para otra), el usuario pregunta por el estado de la relación con un
cliente y las señales chocan, o pide directamente revisar contradicciones.

## Procedimiento

1. **Detecta** con `detectar_contradicciones` (filtra por cliente si aplica).
   La herramienta agrupa los recuerdos del mismo tema, enfrenta las señales
   opuestas y muestra autor, hora y archivo de cada versión.
2. **Presenta las dos versiones SIN tomar partido.** Ninguna es mentira: cada
   KAM vio su pedazo de la realidad. Cita fuente y hora de cada lado — la
   historia inmutable del cerebro es la que permite saber quién dijo qué y
   cuándo.
3. **Lleva el caso a la mesa redonda**: los autores exponen su versión y el
   equipo busca la verdad operativa. Casi nunca gana uno solo — la verdad
   suele tener matices ("quemado en aseo y creciendo en cosmética").
4. **Registra el veredicto** con `resolver_contradiccion`: cliente, tema, qué
   se decidió y por qué, y quién lo decidió. El acta queda con el sello ⚖️.
5. **Verifica el gobierno**: desde ese momento, quien pregunte por el cliente
   recibe primero el veredicto, y las versiones anteriores quedan marcadas
   como resueltas.

## Regla de gobierno

La IA detecta; el equipo decide; el acta manda. Nunca dejes que el asistente
"elija" una versión por su cuenta: el árbitro del conocimiento compartido es
humano, siempre.
