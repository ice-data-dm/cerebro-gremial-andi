---
name: ritmo-diario
description: La danza de las 7:00 - la rutina programada que sincroniza al equipo cada mañana con un informe de un minuto (lo de ayer por cliente y unidad + contradicciones abiertas). Usar cuando el usuario quiera programar su rutina diaria del cerebro o pida su informe matinal.
---

# Ritmo diario — la danza de las 7:00

Las abejas lo llaman danza; nosotros, el comité de las 7:00 sin reunión. La
detección de conflictos deja de ser un accidente y se vuelve un ritual diario.

## Cuándo se dispara

El usuario quiere programar su rutina matinal del cerebro, pide "mi informe de
la mañana", o pregunta cómo mantenerse sincronizado con el equipo.

## Para programar la rutina (una vez)

Guía al usuario a crear una tarea programada en su Claude (corre en la nube
aunque el computador esté apagado) con este texto:

> «Cada mañana a las 7:00, consulta el cerebro corporativo y prepárame un
> informe de un minuto: qué registraron mis compañeros ayer, organizado por
> cliente y por unidad, y qué contradicciones siguen abiertas para que las
> resolvamos hoy en la mesa redonda.»

## Para generar el informe (cada mañana, o a demanda)

1. **Actividad de ayer**: `mapa_del_cerebro` para la actividad reciente, y
   `consultar_cliente` de los clientes con movimiento. Organiza por cliente y
   por unidad, en un minuto de lectura: qué se registró, quién y qué cambia.
2. **Conflictos**: `detectar_contradicciones` sin filtro. Las abiertas van
   PRIMERO en el informe, con sus dos fuentes — son la agenda de la mesa
   redonda de hoy.
3. **Pendientes que vencen**: revisa los pendientes con fecha de hoy o vencida
   y nómbralos con su dueño.
4. **Cierre en una frase**: el estado de la colmena ("ayer 9 registros de 4
   unidades; 1 contradicción abierta sobre SuperAndes; 2 pendientes vencen hoy").

## Regla del ritmo

El informe es de UN minuto: si no cabe, sobra detalle, no falta espacio. Lo
que merezca más profundidad se consulta después, con el cerebro abierto.
