# Workflow — OpsCore

IDEA → VALIDACIÓN → DIFERENCIACIÓN → MVP → DISEÑO → ARQUITECTURA → DESARROLLO → QA → CORRECCIÓN → SEGURIDAD/PRIVACIDAD → RELEASE CANDIDATE → GOOGLE PLAY → TEST CERRADO → PUBLICACIÓN → POST-LANZAMIENTO → MONETIZACIÓN.

Bucle obligatorio: desarrollar → probar → detectar → corregir → volver a probar.

## Prioridad
1. Utilidad real en campo.
2. Simplicidad.
3. Estabilidad.
4. UX móvil.
5. Bajo coste.
6. Velocidad de lanzamiento.

No añadir backend o servicios de pago hasta que el MVP local esté validado.

## Fábrica de apps TheBoltLab

Aplicar una infraestructura común para acelerar desarrollo, evitar repetir trabajo y mantener continuidad entre Chat, Work, Codex y GitHub.

- Reutilizar plantilla Android/Compose, navegación, tema, privacidad, permisos, manejo de errores y estructura base cuando sea razonable.
- Reutilizar workflows de CI, tests, lint, runtime smoke, APK beta, AAB y mantenimiento.
- Mantener `PRODUCT.md`, `WORKFLOW.md`, `AGENTS.md` y `STATUS.md` como fuentes de continuidad.
- Cuando el usuario indique que una versión visual “me gusta”, “está aprobada” o pida “congelar diseño”, crear un punto de referencia estable/tag y no alterar estructura, iconos, navegación o UX aprobada salvo petición expresa o corrección necesaria.
- Priorizar reutilización y cambios incrementales antes que reconstrucciones innecesarias.

## Política GitHub: limpieza sin perder velocidad

GitHub debe mantenerse lo más limpio y ligero posible, pero nunca a costa de perder continuidad ni obligar a reconstruir APKs o dependencias sin necesidad.

- Conservar caché Gradle/Android útil para builds incrementales.
- No borrar toda la caché de forma sistemática.
- Eliminar solo cachés antiguas, duplicadas, incompatibles u obsoletas.
- Mantener artefactos temporales de GitHub Actions con retención corta.
- No acumular APK, AAB o ZIP antiguos en GitHub.
- Archivar versiones importantes, APK, AAB y ZIP de respaldo en el Drive maestro de TheBoltLab.
- Conservar tags/releases importantes y puntos de restauración.
- Eliminar ramas antiguas ya fusionadas cuando sea seguro.
- Antes de borrar algo difícil de reconstruir, asegurar una copia o punto de restauración.
- Automatizar limpieza periódica para evitar alcanzar de nuevo los límites de almacenamiento.

Objetivo operativo: máxima velocidad de desarrollo + GitHub limpio + builds incrementales rápidos + cero pérdidas de trabajo + mínima reconstrucción innecesaria.

