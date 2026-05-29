# 🎣 NotFish: Diseño Conceptual Antifraude Basado en IA

## 🎯 Resumen del Proyecto
NotFish es un diseño arquitectónico conceptual para una extensión de navegador orientada a la protección proactiva del usuario final. Su objetivo principal es identificar, alertar y mitigar campañas de phishing e ingeniería social en tiempo real utilizando capacidades teóricas de Inteligencia Artificial.

## 🧠 Lógica de Detección (El "Motor" Conceptual)
A diferencia de las listas negras tradicionales basadas en reputación estática, NotFish se diseñó para evaluar atributos dinámicos en las páginas web:
* **Análisis Heurístico del DOM:** Evaluación de la estructura de la página para detectar formularios engañosos u ocultos.
* **Procesamiento de Lenguaje Natural (NLP):** Detección de sentido de urgencia o coerción en el texto del sitio (tácticas clásicas de manipulación).
* **Verificación de Entidades:** Análisis de anomalías visuales y similitud tipográfica (ataques homográficos) en la URL.

## 📐 Arquitectura Propuesta
El flujo lógico de la herramienta operaría en 3 fases:
1. **Inspección de Borde:** La extensión captura la solicitud HTTP/HTTPS y el contenido renderizado por el usuario.
2. **Inferencia de IA:** Se extraen las características clave de la URL y el código fuente para ser procesadas por un modelo de clasificación de riesgos.
3. **Respuesta Activa:** Si el umbral de riesgo supera el límite de tolerancia, se bloquea la navegación y se despliega una pantalla de advertencia educativa.

## 📄 Documentación y Evidencia Académica
Este repositorio contiene los artefactos de investigación y elementos visuales desarrollados para la fundamentación del proyecto:

* 📁 **[Reporte de Desarrollo e Investigación](./docs/)**: Documentación detallando el planteamiento del problema, la viabilidad técnica y el impacto esperado de la herramienta.
* 🖼️ **[Diseño Visual y Conceptos](./assets/)**: Material gráfico asociado a la propuesta.

> **Nota:** Este proyecto se presenta actualmente como un caso de estudio y diseño lógico de arquitecturas defensivas orientadas a la concientización en seguridad (Security Awareness).
