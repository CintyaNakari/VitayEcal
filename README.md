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
 [sistema de seguimiento de problemas en GitHub](https://www.youtube.com/watch?v=aZBwFWfgOTI)
