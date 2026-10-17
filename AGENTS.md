# AGENTS.md — BoltLabHub

- GitHub es la fuente de verdad.
- No inventar estados, versiones ni resultados de CI.
- No guardar tokens en frontend.
- No alterar repos de apps desde el Hub sin autorización explícita.
- Mantener diseño mobile-first.
- Distinguir datos sincronizados de datos manuales.

## Modo BOOST — ejecución prioritaria

Cuando este proyecto se retome desde Chat, Work, Codex o un agente de desarrollo, trabajar con máxima autonomía y velocidad sin sacrificar estabilidad.

- Empezar siempre leyendo `PRODUCT.md`, `WORKFLOW.md`, `AGENTS.md` y `STATUS.md` si existe, y contrastar con el estado real de GitHub.
- Priorizar terminar y cerrar lo ya definido antes de abrir nuevas líneas de producto.
- No detenerse para pedir decisiones técnicas rutinarias, reversibles o investigables.
- Resolver errores evidentes, regresiones, lint, tests, compilación y CI de forma autónoma y seguir avanzando.
- Reutilizar código, componentes, workflows y patrones ya validados en TheBoltLab antes de crear soluciones nuevas.
- Evitar reconstrucciones desde cero cuando el proyecto existente pueda repararse o evolucionar incrementalmente.
- Ejecutar en paralelo solo tareas compatibles: desarrollo, QA, revisión, documentación y preparación de release.
- No modificar un diseño aprobado salvo corrección necesaria o petición expresa.
- Mantener GitHub ligero: limpieza selectiva de caché y artefactos, conservando lo útil para builds incrementales y puntos de restauración.
- No anunciar progreso intermedio innecesario. Avanzar hasta decisión importante, prueba física, coste, riesgo de datos, bloqueo externo real o release candidata.
- Cerca del cierre, priorizar: QA total → corrección → prueba de actualización → APK/AAB → release candidate → test cerrado.
- Actualizar `STATUS.md` al finalizar una sesión relevante.

Objetivo BOOST: máxima velocidad útil, mínima fricción, cero trabajo perdido y foco en llevar cada app a una versión instalable, estable y publicable.
