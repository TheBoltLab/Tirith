# AGENTS.md — TheBoltLab

Instrucciones de continuidad y calidad para agentes de desarrollo.

## Protocolo TheBoltLab Pixel Perfect — referencias visuales aprobadas

Aplicar estas reglas en cualquier tarea que cree o modifique una pantalla Android. Este protocolo complementa las normas existentes; no autoriza rediseños ni cambios funcionales no solicitados.

1. Antes de implementar, leer PRODUCT.md, WORKFLOW.md, STATUS.md, FULL_QUALITY.md y las referencias visuales versionadas que existan. Identificar qué imágenes, capturas y decisiones son las últimas aprobadas para cada pantalla y estilo. Si las referencias no están accesibles, no inventarlas ni afirmar fidelidad verificada: registrar la carencia y solicitar únicamente el recurso imprescindible.
2. Tratar cada diseño aprobado como referencia maestra: respetar composición, posiciones, proporciones, fondos HD, iconos, tipografías, colores, sombras, texturas y jerarquía visual. No reemplazar gráficos aprobados por controles genéricos ni crear diseños alternativos.
3. Distinguir los estilos y modos propios de cada app; no copiar funciones o indicadores de un estilo a otro. Si documentación antigua contradice una aprobación posterior comprobable, prevalece la aprobación posterior; documentar la discrepancia sin suponer nuevos requisitos.
4. Convertir controles visibles en componentes Android funcionales conectados a la lógica real. Conservar navegación, datos, persistencia, sensores, accesibilidad y funciones existentes. No simular valores reales, mapas, señales ni estados de producción.
5. Adaptar solo lo imprescindible a densidad, resolución, orientación, recortes, barras del sistema y áreas seguras del dispositivo. Comprobar vertical y horizontal cuando proceda.
6. Para cambios visuales, obtener capturas REALES de la app ejecutándose en un emulador o dispositivo de resolución objetivo. Compararlas con las referencias aprobadas mediante inspección y, cuando sea posible, superposición, diferencias de píxeles y métricas reproducibles. No confundir una maqueta generada con una captura real.
7. Corregir discrepancias relevantes y repetir pruebas funcionales y visuales. Evitar ciclos y compilaciones redundantes: agrupar correcciones, usar CI existente y conservar evidencias de comparación cuando el entorno lo permita.
8. Antes de declarar terminada una entrega: ejecutar compilación, pruebas y lint disponibles; comprobar flujos principales, ausencia de fallos críticos, compatibilidad de datos y, cuando sea viable, actualización sobre la versión previa. Mantener applicationId, identidad de firma y reglas de distribución existentes.
9. No presentar una APK como definitiva si no está compilada, verificada y suficientemente fiel a las referencias aprobadas. Si falta infraestructura, recursos visuales o pruebas físicas, describir con precisión lo verificado y lo pendiente; no declarar cumplimiento ficticio ni prometer fidelidad absoluta.
10. GitHub es la fuente de verdad. Registrar cambios y estado de validación en el repositorio. AGENTS.md son instrucciones para agentes que las lean: NO ejecuta por sí mismo comparaciones, builds ni pruebas; automatizarlas requiere configurar GitHub Actions por separado. No activar workflows, servicios de pago o costes nuevos sin autorización.
