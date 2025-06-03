# Computación Aplicada

Aquí se presentan los archivos y directorios correspondientes al Trabajo Práctico de la materia **Computación Aplicada**.

Este repositorio contiene todos los recursos solicitados, organizados de forma clara para su revisión y evaluación.

## Integrantes del equipo

- **Lucas Calvetti**  
- **Juan Ignacio González Cervi**  
- **Maia Gallardo Mangiamarchi**  
- **Mateo Pagniez**


### ℹ️ Nota sobre la exclusión del directorio `/proc`

Durante este trabajo de compresión y respaldo de directorios del sistema, **hemos excluido intencionadamente el directorio `/proc`**. A continuación se detalla el motivo de esta decisión:

---

#### 📁 ¿Por qué excluimos `/proc`?

El directorio `/proc` **no contiene archivos persistentes**, como ocurre con `/etc` o `/home`. En su lugar, es un **pseudo-sistema de archivos virtual** generado completamente por el kernel de Linux en tiempo real. Actúa como una **interfaz dinámica** entre el espacio de usuario y:

- La información interna del kernel
- Los procesos en ejecución
- Las configuraciones de hardware
- El estado actual del sistema

---

#### ❌ ¿Por qué no se incluye en las copias de seguridad?

- La información dentro de `/proc` **cambia constantemente** mientras el sistema está en funcionamiento.
- Realizar una copia de seguridad de `/proc` capturaría una **instantánea efímera**, sin valor histórico ni utilidad para restauraciones.
- **Su contenido se genera automáticamente** en cada arranque del sistema.
- Intentar restaurar un `/proc` antiguo podría **corromper el entorno actual**, provocando inestabilidad o errores críticos en el sistema operativo.

---

📌 Por estos motivos, **no es necesario ni recomendable incluir `/proc`** en copias de seguridad tradicionales.
