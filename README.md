# VitayEcal

**Descripción del Proyecto:** Este proyecto busca optimizar las condiciones de los cultivos hidropónicos en el hogar mediante el monitoreo en tiempo real de luz, temperatura, CO2 y humedad. Utilizando la tecnología LoRa, se desarrollará un sistema IoT para proporcionar datos precisos y oportunos sobre el ambiente de cultivo, mejorando la productividad y salud de las plantas.

**Propósito:** Facilitar el monitoreo y gestión eficiente de cultivos hidropónicos en casa, permitiendo a los usuarios mantener condiciones óptimas y mejorar el rendimiento de las plantas.

**Alcance:**
* Sensores: Integración de sensores para medir luz, temperatura, CO2 y humedad.
* Comunicación LoRa: Transmisión de datos a través de módulos LoRa.
* Base de datos: Recopilación y procesamiento de datos en una base de datos.
  
**Tecnologías Utilizadas:**
1. Sensores: MQ-135,Sensor de humedad en tierra,fotoresistencia,DGZZI DS18B20
2. Módulos LoRa: Esp32 Lora.
3. Servicios: MQTT (Protocolo de mensajería basado en estándares),InfluxDB (Base de datos de series temporales), Grafana (Plataforma interactiva) y NodeRed 

## Escenarios de Uso

### Implementación del Sistema:
- **Nodos de Sensores**: Se utilizan sensores para medir parámetros como la humedad, temperatura, CO2 y luz ambiental. Estos sensores están conectados a dispositivos LoRa, que permiten la recolección de datos.
- **Gateway LoRa**: Este dispositivo recoge los datos de los nodos de sensores y los transmite a una red central para su almacenamiento y análisis.
- **Almacenamiento de Datos**: Los datos recopilados se almacenan en una base de datos InfluxDB, que está diseñada para gestionar y consultar datos en tiempo real.
- **Visualización de Datos**: Grafana se utiliza para crear paneles de control interactivos, donde los usuarios pueden monitorear los datos en tiempo real y recibir alertas sobre desviaciones significativas.

## Casos de Uso

### Usuario Final:
- **Descripción**: Un individuo que cultiva plantas hidropónicas en su hogar.
- **Acciones del Sistema**:
  - Monitorea parámetros clave del cultivo en tiempo real.
  - Notifica al usuario sobre cualquier desviación significativa en los parámetros.
- **Respuestas Esperadas**:
  - Visualización de datos en tiempo real a través de paneles de control interactivos.
  - Recepción de alertas para tomar medidas correctivas.

### Proveedor del Servicio:
- **Descripción**: Empresa o individuo encargado de la instalación y soporte técnico del sistema.
- **Acciones del Sistema**:
  - Instala los sensores y configura el sistema de comunicación LoRa.
  - Proporciona soporte técnico y actualizaciones del sistema.
- **Respuestas Esperadas**:
  - Instalación correcta y funcionamiento continuo del sistema.
  - Solución de problemas técnicos y provisión de actualizaciones.

## Limitaciones y Mejoras Futuras

### Limitaciones:
- **Alcance de la Conectividad LoRa**:
  - **Descripción**: Las señales LoRa pueden verse afectadas por obstáculos físicos, limitando su alcance.
  - **Estrategia de Mejora**: Implementar repetidores de señal o explorar alternativas de conectividad para superar estas limitaciones.
- **Precisión de los Sensores**:
  - **Descripción**: La precisión de los sensores puede disminuir con el tiempo y las condiciones de uso.
  - **Estrategia de Mejora**: Desarrollar algoritmos de auto-calibración y utilizar sensores de mayor calidad para mejorar la precisión.
- **Interfaz de Usuario**:
  - **Descripción**: La interfaz actual puede no ser intuitiva para todos los usuarios.
  - **Estrategia de Mejora**: Realizar estudios de usabilidad y rediseñar la interfaz basada en las necesidades de los usuarios finales.

### Mejoras Futuras:
- **Integración con Sistemas de Automatización**:
  - **Requisitos**: Desarrollar interfaces y protocolos para conectar el sistema de monitoreo con otros dispositivos de automatización del hogar.
  - **Estrategia**: Colaborar con fabricantes de dispositivos y crear APIs estándar para una integración fluida.
- **Optimización de la Fuente de Energía**:
  - **Requisitos**: Minimizar la dependencia de las baterías.
  - **Estrategia**: Investigar e implementar una batería para que puedan funcionar tanto los sensores como la bomba de agua que tiene el prototipo.
- **Mejora de la Estructura de la Base**:
  - **Requisitos**: Diseñar una base más robusta y adaptable para los sensores y las plantas.
  - **Estrategia**: Utilizar materiales más resistentes y considerar un diseño modular que permita una mayor estabilidad y flexibilidad en diferentes entornos.


## Contribuciones

¡Nos alegra que estés interesado en contribuir a este proyecto! Aquí encontrarás algunas pautas para hacerlo:

### Reportar problemas
Si encuentras algún error, bug o problema con el proyecto, puedes reportarlo a través de nuestro [sistema de seguimiento de problemas](## Contribuciones

¡Nos alegra que estés interesado en contribuir a este proyecto! Aquí encontrarás algunas pautas para hacerlo:

### Reportar problemas
Si encuentras algún error, bug o problema con el proyecto, puedes reportarlo a través de nuestro [sistema de seguimiento de problemas en GitHub](https://github.com/CintyaNakari/VitayEcal/issues). Por favor, asegúrate de proporcionar la mayor cantidad de detalles posible, incluyendo pasos para reproducir el problema.

### Desarrolladores del proyecto

- Jimenez Hernandez Cintya Nakari
- Cruz Maya Yareli de Jesus
- Hernandez Ariza Josue Emanuel
- Zuñiga Serrano Arantza Yoseline
- Angeles Conteras Wendhi Yesbel 

## Licencia

- El aviso de copyright y este aviso de permiso deben incluirse en todas las copias o partes sustanciales del Software.
- EL SOFTWARE SE PROPORCIONA "TAL CUAL", SIN GARANTÍA DE NINGÚN TIPO, EXPRESA O IMPLÍCITA, INCLUYENDO PERO NO LIMITADO A LAS GARANTÍAS DE COMERCIABILIDAD, IDONEIDAD PARA UN FIN DETERMINADO Y NO INFRACCIÓN. EN NINGÚN CASO LOS AUTORES O TITULARES DE LOS DERECHOS DE AUTOR SERÁN RESPONSABLES DE NINGUNA RECLAMACIÓN, DAÑOS U OTRAS RESPONSABILIDADES, YA SEA EN UNA ACCIÓN DE CONTRATO, AGRAVIO O DE OTRO MODO, DERIVADA DE, FUERA DE O EN CONEXIÓN CON EL SOFTWARE O EL USO U OTROS TRATOS EN EL SOFTWARE.

## Video de funcionalidad
 [funcionamiento del prototipo](https://www.youtube.com/watch?v=aZBwFWfgOTI)
 
## Conclusiones

### Reflexión de Jimenez Hernandez Cintya Nakari:
"Trabajar en el proyecto VitayEcal ha sido una experiencia enriquecedora para mí. Desde el inicio, me di cuenta de la importancia de la tecnología IoT en la agricultura moderna, especialmente en cultivos hidropónicos. La integración de sensores y el uso de LoRa para la transmisión de datos nos ha permitido crear un sistema robusto y eficiente. Esta experiencia me ha enseñado a valorar la precisión y la puntualidad en la recolección de datos, esenciales para mantener condiciones óptimas de cultivo. Espero seguir mejorando mis habilidades en este campo y contribuir a innovaciones futuras en la agricultura tecnológica."

### Reflexión de Cruz Maya Yareli de Jesus:
"Participar en este proyecto me ha permitido comprender mejor los desafíos y las oportunidades en el monitoreo de cultivos hidropónicos. A través de la implementación de diferentes tecnologías, he aprendido sobre la importancia de la precisión en la medición de parámetros como la luz, temperatura, CO2 y humedad. Además, el uso de InfluxDB y Grafana para el almacenamiento y visualización de datos ha sido una parte crucial del proyecto, permitiendo una gestión eficiente y en tiempo real. Estoy agradecida por la oportunidad de trabajar en este proyecto y emocionada por las futuras mejoras que podemos implementar."

### Reflexión de Hernandez Ariza Josue Emanuel:
"Desarrollar el sistema VitayEcal ha sido una experiencia desafiante y gratificante. La implementación de la tecnología LoRa para la transmisión de datos ha sido una de las partes más interesantes del proyecto. A lo largo del desarrollo, he aprendido mucho sobre la importancia de una comunicación eficiente y cómo superar las limitaciones físicas que pueden afectar las señales LoRa. Este proyecto me ha inspirado a seguir explorando soluciones innovadoras en el campo de la agricultura tecnológica y a seguir mejorando nuestros sistemas para un mejor rendimiento."

### Reflexión de Zuñiga Serrano Arantza Yoseline:
"Ser parte del equipo de VitayEcal me ha permitido profundizar en el mundo de la tecnología aplicada a la agricultura. La integración de sensores y el monitoreo en tiempo real son elementos clave que pueden transformar la manera en que cultivamos plantas hidropónicas en casa. Me ha impresionado ver cómo la recopilación y el análisis de datos pueden impactar positivamente en la salud y productividad de las plantas. Estoy orgullosa de lo que hemos logrado hasta ahora y entusiasmada por las mejoras futuras que podemos desarrollar para hacer este sistema aún más efectivo y accesible."

### Reflexión de Angeles Conteras Wendhi Yesbel:
"Trabajar en el proyecto VitayEcal ha sido una experiencia sumamente gratificante para mí. A través del desarrollo de este sistema, he aprendido la importancia de la tecnología IoT y la precisión en la recolección de datos para mantener condiciones óptimas en los cultivos hidropónicos. Además, la utilización de herramientas como NodeRed y Grafana para la visualización de datos en tiempo real ha sido fundamental para proporcionar a los usuarios una experiencia interactiva y eficiente. Estoy emocionada por el potencial de este proyecto y las futuras mejoras que podemos implementar para hacerlo aún más robusto y accesible."

### Referencias bibliograficas
- Leroymerlin.es. [Online]. Available: https://www.leroymerlin.es/ideas-y-consejos/consejos/cultivo-hidroponico-todo-que-debes-saber.html. [Accessed: 29-May-2024].
- V. Urdiales-Ponce and J. Espín-Ortega, “Monitoreo de un sistema hidropónico NFT a escala usando arquitectura arduino (PARTE 1),” Rev. Tecnol. Marcha, vol. 31, no. 2, p. 147, 2018.
- M. A. Z. Aquino, “MANUAL DE HIDROPONIA,” Gob.mx. [Online]. Available: https://www.gob.mx/cms/uploads/attachment/file/232367/Manual_de_hidroponia.pdf. [Accessed: 29-May-2024].
- “ESP32 LoRa Heltec v2 with display – pinout diagram,” EscapeQuotes, 23-Feb-2021. [Online]. Available: https://escapequotes.net/esp32-lora-heltec-v2-with-display-pinout-diagram/. [Accessed: 29-May-2024].
- Usda.gov. [Online]. Available: https://www.nal.usda.gov/farms-and-agricultural-production-systems/hydroponics. [Accessed: 29-May-2024].




