# 🧰 Skills del Cerebro Comercial UNIANDI

Procedimientos comerciales empaquetados como **skills**: instrucciones que un
asistente de IA puede descubrir, instalar y ejecutar. Cada skill vive en
`skills/<identificador>/SKILL.md` con un encabezado (`name`, `description`) y
el procedimiento en el cuerpo.

## Cómo los usa un asistente

- **Desde el conector del cerebro (cualquier Claude):** `listar_skills` muestra
  el catálogo y `obtener_skill` trae el contenido completo con sus
  instrucciones de instalación.
- **Agentes con sistema de archivos (Claude Code, Agent SDK):** guardar el
  SKILL.md en `~/.claude/skills/<identificador>/SKILL.md` lo deja instalado y
  invocable en cualquier sesión.
- **claude.ai:** el procedimiento se aplica en la conversación o se pega en las
  instrucciones de un proyecto.
- **Directo del repositorio (sin conector):**
  `https://raw.githubusercontent.com/ice-data-dm/cerebro-gremial-andi/main/skills/<identificador>/SKILL.md`

## Catálogo

| Skill | Qué hace |
|---|---|
| `consultar-antes-de-decidir` | La disciplina central: consultar el cerebro antes de cualquier decisión comercial |
| `registrar-incidente-completo` | Reportar un incidente con el estándar del CRM (impacto, causa, dueños, cierre) |
| `aprendizaje-de-promociones` | Cerrar una promoción convirtiendo el resultado en aprendizaje reutilizable |
| `alta-de-cliente-completa` | Crear un cliente nuevo con la ficha completa desde la primera conversación |
| `preparar-comite-ejecutivo` | Convertir el digest del CRM en el informe ejecutivo del comité |
