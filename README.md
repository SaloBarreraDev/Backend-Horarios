# 📅 Base de datos de Horarios

Este repositorio actúa como servidor de archivos estáticos para la aplicación **Unexum**, utilizada por los estudiantes de la **UNEXPO-VRB** para la gestión de sus datos académicos.

## 📂 Estructura del Repositorio

Aquí se alojan los archivos JSON que la aplicación consulta y descarga para mantener la información de materias y secciones actualizada sin necesidad de actualizar la app completa en la PlayStore.

### 1. `version_horario.json`
Archivo ligero de metadatos. La app consulta este archivo primero para verificar si existe una nueva versión de los horarios.
- **Contenido:** Número de versión, mensaje de novedades, lapso académico actual y fecha de actualización.

### 2. `base_datos.json`
Archivo principal que contiene toda la estructura de asignaturas, secciones, aulas y profesores.
- **Descarga:** Solo se descarga si la versión en `version_horario.json` es superior a la instalada en el dispositivo.

## 🔄 Flujo de Actualización

El sistema funciona bajo la siguiente arquitectura:
1.  La app intenta conectar con este repositorio.
2.  Compara el número de versión local vs. remoto.
3.  Si hay una versión nueva, descarga el JSON crudo (Raw) desde aquí.
4.  La app se actualiza automáticamente mostrando el nuevo lapso académico.

---
**Desarrollado por:** Salomón Barrera.

*Proyecto independiente para la comunidad estudiantil de la UNEXPO-VRB.*
