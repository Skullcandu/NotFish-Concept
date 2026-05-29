# 📄 Informe de Desarrollo: NotFish

* **Proyecto:** NotFish - Extensión de Navegador con IA para la Detección de Phishing
* **Autor:** Daniel Neira
* **Área:** Ingeniería en Ciberseguridad, AIEP

---

## 1. Introducción y Problema
El phishing sigue siendo una amenaza crítica. Las soluciones tradicionales como las listas negras son reactivas y lentas. El proyecto **NotFish** aborda esta brecha mediante una extensión de navegador que utiliza Inteligencia Artificial para analizar sitios web en tiempo real. A diferencia de las herramientas pasivas, NotFish evalúa activamente cada sitio, pudiendo detectar amenazas de "día cero" (ataques completamente nuevos) antes de que sean reportados a las bases de datos globales.

## 2. Arquitectura y Modelo de IA
El sistema NotFish se basa en una arquitectura híbrida. Un **Componente de Cliente (Extensión)** liviano se ejecuta en el navegador del usuario, monitoreando las URLs y el contenido del DOM. Este cliente se comunica bidireccionalmente con el **Núcleo de IA**.

El núcleo utiliza un modelo de Machine Learning entrenado para identificar patrones de suplantación de identidad. La fase más crucial del desarrollo fue la *Ingeniería de Características (Feature Engineering)*, donde el sitio web se vectoriza en datos procesables para la IA. El modelo evalúa más de 50 características, agrupadas en tres categorías principales:

* 🔗 **Análisis de URL:** Evalúa la longitud, la implementación estricta de HTTPS, la antigüedad del dominio y busca patrones de *typosquatting* (ej. `G0ogle.com`).
* 📝 **Análisis de Contenido (NLP/DOM):** Mediante Procesamiento de Lenguaje Natural, busca frases de "urgencia" (ej. *"cuenta suspendida"*) y analiza la estructura oculta de los formularios de contraseña y la legitimidad de sus enlaces de redirección.
* 👁️ **Análisis Visual (CV):** A través de Computer Vision, detecta la "similitud de plantilla", comparando visualmente si un sitio sospechoso está imitando la paleta de colores, el logo y el diseño de un sitio legítimo conocido (ej. una entidad bancaria).

## 3. UI/UX y Validación (Respuesta Activa)
Si el modelo de IA asigna una puntuación de riesgo alta, NotFish interrumpe la conexión y bloquea la página desplegando una alerta intersticial clara. Esta pantalla advierte al usuario del peligro de forma educativa antes de que ingrese cualquier credencial. 

El desarrollo teórico se centró en métricas de validación estrictas, apuntando a una **tasa de detección de amenazas (True Positives) superior al 99%**, aplicando modelos de ajuste para minimizar a su vez los falsos positivos (bloqueo erróneo de sitios legítimos).
