---
name: difundir-comunicados
description: Construir el Excel del equipo desde las tarjetas de KAMs y preparar comunicaciones por correo (comunicados o misiones individuales) usando el Gmail nativo de Claude - SIEMPRE como borradores que el usuario revisa y envía. Usar cuando el facilitador quiera escribirle a uno o a todos los miembros del equipo, o repartir misiones del taller por correo.
---

# Difundir comunicados al equipo

El cerebro conoce a su gente (nombre, unidad, correo). Este skill convierte ese
directorio en comunicación directa: un Excel del equipo y borradores de correo
personalizados — comunicados generales o misiones individuales del taller.

## Requisitos

El conector del cerebro («Cerebro Gremial ANDI») y el conector nativo de
**Gmail** activos en la conversación. Sin Gmail conectado, este skill solo
puede producir el Excel y los textos.

## Regla dura (no negociable)

**Todo correo se prepara como BORRADOR en Gmail. Nunca se envía directamente.**
El usuario revisa cada borrador en su Gmail y decide enviarlo. Los correos del
directorio son datos personales del ejercicio: solo se usan para comunicaciones
del programa (ver PRIVACIDAD.md) y jamás se copian a destinatarios externos.

## Procedimiento

### 1. El directorio y el Excel
1. Trae el directorio completo con `listar_equipo`: devuelve la tabla y un
   bloque CSV con nombre, unidad, correo, cargo y foco de cada KAM registrado.
2. Construye el archivo: genera un **Excel** (o CSV si el entorno no produce
   xlsx) con esas columnas, una fila por persona, y entrégalo al usuario.
3. Señala los registros sin correo (tarjetas anteriores al campo obligatorio):
   esas personas deben volver a presentarse para completarlo.

### 2. Comunicado general (a todos o a un subconjunto)
1. Pregunta al usuario (si no lo dijo): a quiénes (todos, una unidad, nombres)
   y el mensaje de fondo.
2. Redacta el comunicado una vez, con asunto estándar:
   `🧠 La Colmena · {tema}` — y personaliza el saludo con el nombre de pila.
3. Crea con Gmail **un borrador por destinatario** (nunca un solo correo con
   todos en copia: los correos de los participantes no se exponen entre sí).
4. Reporta: cuántos borradores quedaron creados y para quién — y recuérdale al
   usuario que los revise y envíe desde su Gmail.

### 3. Modo taller: misiones por correo
Para repartir tareas que los KAMs siguen desde su bandeja y ejecutan contra el
cerebro (registrar, consultar), cada borrador lleva:

- **Asunto:** `🧠 La Colmena · Tu misión, {nombre}`
- **Cuerpo:** saludo por nombre + la misión en imperativo claro + el cierre:
  "Díctale la misión a tu Claude tal como está escrita. Él sabe qué herramienta
  del cerebro usar. Cuando termines, guarda silencio y espera la señal."

**Las dos misiones contradictorias del choque** (una por correo, a UN KAM de
cada unidad, sin que sepan del otro):

> **Para un KAM de Aseo del Hogar:** "Registra este incidente en el cerebro:
> SuperAndes está quemado. Jorge Iván Restrepo, el comprador de aseo, está
> molesto por el agotado del Detergente Brillante de 2 kg y congeló las órdenes
> del mes. Riesgo estimado: $180 millones de venta del mes. Estado: abierto."

> **Para un KAM de Cuidado Personal:** "Registra esta visita en el cerebro:
> SuperAndes está perfecto. Me reuní con Tatiana Bermúdez, la compradora de
> cuidado personal, y está feliz con la rotación de la marca Esencia: confirmó
> que ampliará los espacios el próximo trimestre. Acuerdo: presentarle la
> propuesta de surtido ampliado en la próxima cita."

Las demás misiones salen de las tarjetas del grupo del KAM (según su unidad).
Después del choque, la resolución se hace en vivo con
`detectar_contradicciones` y `resolver_contradiccion` — no por correo.

## Antipatrones

- Enviar en vez de crear borradores (prohibido siempre).
- Un solo correo con 30 personas en copia.
- Usar los correos para cualquier cosa ajena al programa.
- Inventar correos: solo los del directorio; sin correo en la tarjeta, no hay
  borrador.
