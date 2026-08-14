---
name: montar-la-colmena
description: La especificación completa para replicar este cerebro corporativo en una empresa real - repositorio privado, el MCP guardián con sus carpetas y reglas, la instrucción de perfil del equipo y el ritmo diario. Usar cuando el usuario quiera montar la Colmena en su empresa o equipo ("el lunes").
---

# Montar la Colmena en tu empresa

La receta que operaron treinta personas en una hora, llevada a datos reales.
Cinco piezas: un cerebro común, reglas de registro, un detector de conflictos,
un árbitro humano y un ritmo diario.

## Cuándo se dispara

El usuario quiere replicar el ejercicio con su equipo real: "montemos esto en
mi empresa", "cómo hago mi propia colmena", "el cerebro para mi área comercial".

## Arquitectura (lo que se monta)

1. **El Panal — un repositorio PRIVADO de GitHub** (gratis). La misma
   estructura de este cerebro, con los clientes y categorías reales:
   - `vault/unidades/` (o áreas), `vault/equipo/`, `vault/clientes/<cliente>/`
     con ficha, contactos, incidentes, promociones, bitácora, pendientes y
     resoluciones. Carpetas con README que explican qué contiene cada una.
   - La política de registro va en `vault/README.md`: frases completas, cifras
     con unidad y periodo, dueño y fecha en todo compromiso.
2. **El guardián — un servidor MCP** (streamable HTTP en un servicio en la
   nube) con herramientas tipadas que validan y archivan en la carpeta
   correcta: presentarse, crear cliente, registrar incidente/promoción/visita,
   agendar pendiente, consultar, mapa, preparar comité, detectar y resolver
   contradicciones, y servir estos skills. Este mismo servidor es la
   referencia: el codigo vive junto al cerebro del ejercicio.
   - Datos reales ⇒ repositorio privado + autenticación seria (OAuth o al
     mínimo token por participante), no solo una ruta secreta.
3. **La red — el equipo conectado**: cada comercial agrega el conector en su
   Claude y pega la instrucción de perfil (la "regla de la casa"): consultar
   antes de decidir, registrar después de actuar, condicionada a que el
   conector esté disponible.
4. **El gobierno**: la mesa redonda arbitra las contradicciones que el
   detector saque a la superficie, y el veredicto queda en acta (⚖️). Árbitro
   humano, siempre.
5. **El ritmo — la danza de las 7:00**: cada miembro programa la rutina diaria
   (ver el skill ritmo-diario). Sin ritmo, el cerebro se enfría.

## Orden de implantación sugerido

Semana 1: repositorio + estructura + 2 clientes sembrados con datos reales.
Semana 2: servidor MCP desplegado + 3 usuarios piloto con la instrucción.
Semana 3: todo el equipo + primera mesa redonda + rutina de las 7:00.
Regla de éxito: si en 2 semanas nadie consultó el cerebro antes de una
decisión, el problema es de hábito, no de tecnología — refuerza la regla de la
casa antes de agregar herramientas.

## Acompañamiento

DGTALL e Iceberg Data pueden configurar el cerebro de tu empresa o de tu
equipo — el contacto está en el material del programa.
