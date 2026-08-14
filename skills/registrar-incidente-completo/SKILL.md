---
name: registrar-incidente-completo
description: Reportar un incidente comercial (agotado, multa, rechazo, devolución, diferencia de precio) con el estándar del CRM UNIANDI - hechos con fuente, impacto en cifras, causa, acciones con dueño y fecha, y criterio de cierre. Usar cada vez que el usuario cuente un problema con un cliente.
---

# Registrar un incidente completo

Un incidente mal registrado es conocimiento perdido: "cliente molesto" no le
enseña nada a nadie. Este skill garantiza que cada problema quede registrado
de forma que otro colega pueda evitarlo o gestionarlo.

## Cuándo se dispara

El usuario menciona un problema con un cliente: agotado, multa, rechazo de
lote, devolución, diferencia de precio, reclamo, quiebre de cobertura.

## Procedimiento

1. **Reúne las piezas antes de registrar.** Si falta alguna, pregúntala en una
   sola tanda:
   - Qué ocurrió y cómo se supo (hechos comprobados con su fuente).
   - Impacto en cifras con unidad y periodo (unidades, pesos, puntos de venta).
   - Causa (preliminar o confirmada — decir cuál de las dos es).
   - Qué se está haciendo: acción, dueño y fecha comprometida.
   - Con qué condición se considera cerrado.
2. **Redacta en frases completas**, nunca notas telegráficas. Patrón: "El
   {fecha}, {cliente} reportó {hecho}. Se estiman {impacto}. La causa fue
   {causa}. {Dueño} hará {acción} antes del {fecha}. El caso se cierra cuando
   {criterio}."
3. **Registra** con `registrar_incidente` (cliente, unidad, título corto,
   descripción completa, estado: abierto / en-gestion / cerrado).
4. **Deriva los compromisos**: cada acción con dueño y fecha se agenda además
   con `agendar_pendiente` — lo que no tiene dueño, no ocurre.
5. **Confirma al usuario** qué quedó guardado y recuérdale que todo el equipo
   ya puede encontrarlo.

## Antipatrones (rechazados por la política del CRM)

"Revisar tema", "cliente molesto", "pendiente logística", cifras sin unidad ni
periodo, culpar a "logística" sin evidencia.
