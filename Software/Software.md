# Tecnologías Utilizadas:

## **Lenguajes utilizados:**

* **C++:** Es un lenguaje de programación de propósito general que se utiliza ampliamente para el desarrollo de aplicaciones de software. Fue desarrollado por Bjarne Stroustrup en los años 1980 como una extensión del lenguaje C, incorporando características de programación orientada a objetos (OOP).
* **JavaScript:** Es un lenguaje de programación ampliamente utilizado tanto en el desarrollo web como en otros contextos de programación. Originalmente desarrollado para ejecutarse en navegadores web, JavaScript ahora también se utiliza en entornos de servidor a través de plataformas como Node.js.

## **Bibliotecas:**
Para la programación del código tanto del transmisor como del receptor, se utilizó el microcontrolador Arduino.En el desarrollo del código del receptor, se incluyeron varias bibliotecas esenciales. A continuación, se detallan algunas de ellas:

* **heltec.h:** Esta biblioteca es específica para dispositivos de la marca Heltec, como las placas WiFi LoRa de la serie ESP32. Proporciona una interfaz fácil de usar para configurar y controlar las características del hardware, como la pantalla OLED integrada y el módulo LoRa.
* **WiFi.h:** Esta biblioteca proporciona las funciones necesarias para establecer y administrar conexiones Wi-Fi en dispositivos ESP32. Permite conectar el dispositivo a una red Wi-Fi existente y realizar operaciones de comunicación a través de ella.
* **PubSubClient.h:** Esta biblioteca implementa el protocolo de cliente MQTT para dispositivos ESP32. MQTT es un protocolo ligero de mensajería diseñado para la comunicación entre dispositivos conectados a Internet de las Cosas (IoT). PubSubClient simplifica la publicación y suscripción a temas MQTT en aplicaciones de IoT.

En el desarrollo del código del transmisor, se incluyeron varias bibliotecas esenciales. A continuación, se detallan algunas de ellas:

* **heltec.h:** Esta biblioteca es específica para dispositivos de la marca Heltec, como las placas WiFi LoRa de la serie ESP32. Proporciona una interfaz fácil de usar para configurar y controlar las características del hardware, como la pantalla OLED integrada y el módulo LoRa.
* **OneWire.h:** Esta biblioteca permite la comunicación a través del bus OneWire, que es un protocolo de comunicación serial diseñado para la conexión de dispositivos a través de un solo conductor. 
* **DallasTemperature.h:** Esta biblioteca se construye sobre la biblioteca OneWire y proporciona funciones específicas para interactuar con los sensores de temperatura de Dallas Semiconductor, como el DS18B20. Facilita la lectura de temperaturas y el manejo de múltiples sensores en el mismo bus OneWire.

## **Herramientas:**
Utilizamos las siguientes herramientas:
* **Node-RED:** Herramienta de programación visual basada en flujos para la integración de hardware y software, utilizada para el procesamiento y visualización en tiempo real de los datos.
[![Node-red](https://i.postimg.cc/GpvjMSBk/200px-Node-red-icon.png)](https://postimg.cc/yJY9xjyd)
* **InfluxDB:** Base de datos de series temporales eficiente para el almacenamiento de datos recolectados por los sensores.
* **Grafana:** Plataforma de visualización gráfica y dinámica para crear paneles de control que permiten la visualización detallada de las condiciones ambientales del cultivo.
* **MQTT:**  Es un protocolo de mensajería ligero y de bajo consumo de ancho de banda diseñado para dispositivos con recursos limitados y redes con ancho de banda limitado.

