---
name: alta-de-cliente-completa
description: Crear un cliente nuevo en el CRM UNIANDI con la ficha completa desde la primera conversación - canal, ciudad, contacto, condiciones comerciales y contexto. Usar cuando el usuario mencione un cliente o prospecto que no existe en el CRM.
---

# Alta de cliente completa

Un cliente creado a medias es un cliente que nadie más puede atender. Este
skill garantiza que todo cliente entre al CRM con lo que un colega necesitaría
para sentarse con él mañana.

## Cuándo se dispara

El usuario menciona un cliente o prospecto que no aparece en el CRM (la
herramienta de registro lo rechazará con "no está en el CRM"), o pide
explícitamente crear uno.

## Procedimiento

1. **Verifica que de verdad no exista**: consulta el panorama
   (`consultar_cliente`) con el nombre y sus variantes — puede estar con otro
   identificador. Crear duplicados fragmenta la memoria.
2. **Reúne los 4 datos obligatorios** (pregunta los que falten en una sola
   tanda, con ejemplos para que el usuario responda rápido):
   - **Canal**: gran superficie, tiendas de barrio, mayorista, droguerías,
     institucional, descuento duro, e-commerce…
   - **Ciudad o región** de operación.
   - **Contacto principal**: nombre y rol.
   - **Condiciones comerciales**: plazo de pago, márgenes o descuentos,
     logística, particularidades (multas, ventanas, requisitos).
3. **Suma contexto si el usuario lo tiene** (tamaño, historia, oportunidad) en
   el campo de notas — es opcional, no lo bloquees por esto.
4. **Crea** con `crear_cliente` y confirma el identificador que devuelve: con
   ese identificador se registran los incidentes, promociones, visitas y
   pendientes del cliente de ahí en adelante.
5. **Primer registro inmediato**: si el alta nació de una visita o una
   negociación, regístrala de una vez — un cliente sin historial es solo un
   nombre.

## Antipatrón

Crear el cliente "para no perder el dato" con condiciones vacías o inventadas.
Si el usuario no sabe una condición, se registra la mejor información
disponible diciendo que está por confirmar — nunca en silencio.
