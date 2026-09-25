# Matriz de Decisión: Selección de Framework Móvil

**Instrucciones de uso:**

1. Lee detenidamente el archivo [requerimientos_proyectos.json](./requerimientos_proyectos.json) .
2. Asigna una **Calificación (del 1 al 5)** a cada framework por cada criterio, donde 1 es "Deficiente/Inviable" y 5 es "Excelente/Óptimo".
3. Multiplica la Calificación por el **Peso** asignado para obtener el **Puntaje Ponderado**.
4. Suma los puntajes ponderados en la última fila para descubrir el framework ganador.

| Criterios de Evaluación | Peso (1-5) | Desarrollo Nativo (Swift/Kotlin) | React Native | Flutter |
| :--- | :---: | :--- | :--- | :--- |
| **1. Curva de Aprendizaje / Fit con el Equipo**<br>*(Considerar stack actual del equipo)* | **5** | Calificación: **1**<br>Puntaje: **5** | Calificación: **5**<br>Puntaje: **25** | Calificación: **3**<br>Puntaje:**15** |
| **2. Time-to-Market**<br>*(Velocidad para lanzar en iOS y Android en 3 meses)* | **5** | Calificación: **1**<br>Puntaje:**5** | Calificación: **5**<br>Puntaje:**25** | Calificación: **4**<br>Puntaje:**20** |
| **3. Capacidades de Hardware (GPS en 2do plano)**<br>*(Acceso a APIs del sistema de forma eficiente)* | **4** | Calificación: **5**<br>Puntaje:**20** | Calificación: **4**<br>Puntaje:**16** | Calificación: **4**<br>Puntaje:**16** |
| **4. Rendimiento de UI**<br>*(Animaciones de mapas y fluidez general)* | **3** | Calificación: **15**<br>Puntaje:**15** | Calificación: **4**<br>Puntaje:**12** | Calificación: **5**<br>Puntaje:**15** |
| **5. Ecosistema y Mantenimiento**<br>*(Disponibilidad de librerías para cámara, mapas, etc.)* | **3** | Calificación: **5**<br>Puntaje:**15** | Calificación: **5**<br>Puntaje:**15** | Calificación: **4**<br>Puntaje:**12** |
| **PUNTAJE TOTAL** | -- | **Total Nativo**: **60** | **Total React Native**: **93** | **Total Flutter**: **78** |

---

## Validación de Viabilidad Tecnológica

Basado en el ganador de la matriz, investiga en la documentación oficial o repositorios comunitarios populares (NPM, pub.dev, CocoaPods, etc.) los paquetes que resolverán los requerimientos críticos.

**Framework Ganador:** React Native

**1. Solución para GPS en segundo plano:**

* Nombre de la librería/paquete: @transistorsoft/react-native-background-geolocation (o bien, expo-location si se usa el ecosistema Expo).
* Enlace oficial: [React Native Background Geolocation - NPM](https://www.npmjs.com/package/@react-native-community/geolocation)
* ¿Por qué es viable?:

**2. Solución para Cámara (QR y Evidencia):**

* Nombre de la librería/paquete: react-native-vision-camera (para alto rendimiento) o expo-camera.
* Enlace oficial: [React Native Vision Camera - NPM](https://www.npmjs.com/package/react-native-vision-camera)
* ¿Por qué es viable?: Proporciona un rendimiento fluido de fotogramas por segundo necesario para el escaneo veloz de códigos QR de paquetes y permite capturar fotografías con compresión inmediata para subirlas de forma asíncrona como evidencia de entrega.

---

## Dictamen Final (Resumen Ejecutivo)

Tras un riguroso análisis técnico basado en una matriz de decisión ponderada, hemos seleccionado React Native como la tecnología oficial para el desarrollo del MVP de GeoTracker Pro.

Dada la estricta ventana de Time-to-Market de 3 meses y un presupuesto de contratación restringido, optar por un desarrollo nativo puro (Swift/Kotlin) habría significado duplicar los costos y esfuerzos en dos bases de código distintas, superando con creces nuestro límite temporal. Por otro lado, aunque alternativas como Flutter son potentes, nuestro equipo cuenta con un sólido dominio de JavaScript y React.js, lo que nos otorga una curva de aprendizaje nula y garantiza productividad desde la primera semana sin necesidad de incurrir en costosas contrataciones externas o capacitación intensiva.

Elegir React Native protege nuestro ROI al maximizar la reutilización de código (90% compartido entre iOS y Android) y mitiga los riesgos técnicos asociados al GPS en segundo plano y la lectura de códigos QR mediante el uso de librerías nativas probadas en producción. Esta decisión equilibra con precisión milimétrica la viabilidad financiera de la startup con la excelencia técnica requerida para el éxito comercial del proyecto.

Atentamente,

Líder Técnico (Tech Lead), Abdiel Mendez
