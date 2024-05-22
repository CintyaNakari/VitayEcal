Contiene información sobre el hardware utilizado en el proyecto.



  ## Componentes Utilizados:

  Lista de los componentes de hardware utilizados en el proyecto, incluyendo placas de desarrollo, sensores, actuadores, etc.

- Sensor de humedad con bomba de agua
- sensor de temperatura
- Sensor de calidad de aire
- Fotoresistencia
- Esp32 Lora

 ## Esquemáticos:

Esquemáticos y diagramas de conexión (Detallado y claro) de los componentes de hardware utilizados en el proyecto.

 ## Configuración:

Instrucciones para la configuración física de los componentes de hardware y su conexión entre sí.

Interconexión de Red Cableada e Inalámbrica (Topologia Logica y Fisica, con direccionamiento en los ambientes LoRa, Bluethoo, NFC, GPS, Infrarrojo y Wi-Fi) :
Cableada:

Descripción de la configuración de la red cableada utilizada en el proyecto, incluyendo el tipo de cableado, dispositivos de red y su configuración.

Inalámbrica:

Descripción de la configuración de la red inalámbrica utilizada en el proyecto, incluyendo el tipo de tecnología inalámbrica (Wi-Fi, Bluetooth, Zigbee, etc.), dispositivos de red inalámbrica y su configuración.

 ## Funcionabilidad:
 
 ## Escenarios de Uso:

Evidencia Fotografica y video de escenarios de uso del proyecto, demostrando cómo interactúa el usuario final con el sistema y qué resultados se pueden esperar (datos hisotoricos en la base de datos).

 ## Casos de Uso (para Usuario Final, Administrador ó Proveedor del Servicio):

Usuario Final
- Monitoreo de Parámetros en Tiempo Real:

  - Acción: El usuario abre la aplicación web o móvil.
  - Respuesta: El sistema muestra una interfaz con los datos actuales de luz, temperatura, CO2 y humedad.
  - Resultado Esperado: El usuario puede ver gráficos y lecturas en tiempo real de los parámetros ambientales del cultivo hidropónico.

- Historial de Datos:

  - Acción: El usuario selecciona una opción para ver el historial de datos.
  - Respuesta: El sistema despliega gráficos históricos de los parámetros seleccionados.
  - Resultado Esperado: El usuario puede analizar las tendencias y cambios en las condiciones ambientales a lo largo del tiempo.

- Alertas y Notificaciones:

  - Acción: El usuario configura alertas para ciertos umbrales de parámetros (ej., temperatura alta, baja humedad).
  - Respuesta: El sistema envía notificaciones (push o email) cuando se superan estos umbrales.
  - Resultado Esperado: El usuario recibe alertas en tiempo real, permitiéndole tomar medidas correctivas rápidamente.

ADMINISTRADOR
- Gestión de Dispositivos:

    - Acción: El administrador accede a una interfaz de gestión de dispositivos.
    - Respuesta: El sistema muestra una lista de todos los sensores y módulos LoRa conectados.
    - Resultado Esperado: El administrador puede agregar, eliminar o reconfigurar dispositivos según sea necesario.

- Configuración de la Red LoRa:

    - Acción: El administrador ajusta los parámetros de la red LoRa (frecuencia, potencia de transmisión).
    - Respuesta: El sistema aplica los nuevos ajustes a todos los dispositivos conectados.
    - Resultado Esperado: La red LoRa se optimiza para mejorar la transmisión de datos y la cobertura.

- Monitoreo de Rendimiento del Sistema:

    - Acción: El administrador revisa el rendimiento del sistema a través de métricas y logs.
    - Respuesta: El sistema muestra estadísticas de rendimiento y registros de eventos.
    - Resultado Esperado: El administrador puede identificar y solucionar problemas técnicos de manera proactiva.

PROVEEDOR DEL SERVICIO

- Implementación y Soporte:

    - Acción: El proveedor configura el sistema en nuevas instalaciones de usuarios.
    - Respuesta: El sistema guía al proveedor a través del proceso de instalación y configuración inicial.
    - Resultado Esperado: El sistema se implementa correctamente y el proveedor puede ofrecer soporte técnico continuo.

- Actualización de Software y Firmware:

    - Acción: El proveedor despliega actualizaciones de software y firmware.
    - Respuesta: El sistema actualiza automáticamente todos los componentes relevantes.
    - Resultado Esperado: El sistema se mantiene actualizado con las últimas características y correcciones de seguridad.

- Escalabilidad del Sistema:

    - Acción: El proveedor planifica la expansión del sistema a múltiples ubicaciones o usuarios.
    - Respuesta: El sistema se adapta para manejar una mayor cantidad de dispositivos y datos.
    - Resultado Esperado: El sistema soporta la expansión sin degradación del rendimiento.

 ## Limitaciones y Mejoras Futuras:


- Alcance de Cobertura de LoRa:

    - Limitación: La cobertura de la señal LoRa puede verse afectada por obstáculos físicos y la distancia.
    - Requisito: Mejorar la infraestructura de repetidores y gateways para asegurar una cobertura más amplia.

- Precisión de los Sensores:

    - Limitación: Los sensores utilizados pueden tener limitaciones en precisión y rango de medición.
    - Requisito: Integrar sensores de mayor precisión y calibrarlos regularmente para asegurar datos fiables.

- Consumo Energético:

    - Limitación: Aunque LoRa es de bajo consumo, los sensores y el microcontrolador aún requieren una fuente de energía constante.
    - Requisito: Investigar y desarrollar soluciones energéticamente eficientes, como el uso de energía solar.


MEJORAS CONTINUAS
- Mejora en la Interfaz de Usuario:

    - Mejora: Desarrollar una interfaz de usuario más intuitiva y visualmente atractiva.
    - Estrategia: Realizar estudios de usabilidad y aplicar diseño centrado en el usuario.

- Integración con Otros Sistemas Domóticos:

    - Mejora: Integrar el sistema con plataformas de hogar inteligente como Google Home o Amazon Alexa.
    - Estrategia: Desarrollar APIs y módulos de integración para interoperabilidad.

- Análisis Predictivo:

    - Mejora: Implementar algoritmos de inteligencia artificial para el análisis predictivo de los datos recolectados.
    - Estrategia: Utilizar técnicas de machine learning para anticipar y optimizar las condiciones de cultivo.

  ## Contribuciones:

    Instrucciones para contribuir al proyecto, incluyendo cómo reportar problemas, enviar solicitudes de extracción y participar en el desarrollo activo.

  ## Licencia:

    Información sobre la licencia del proyecto y los términos de uso para los usuarios y colaboradores.
