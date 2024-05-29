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

[![influx-DB](https://i.postimg.cc/Yq8vfct5/influx-DB-logo-becon-Gmb-H.png)](https://postimg.cc/crg10bgh)

* **Grafana:** Plataforma de visualización gráfica y dinámica para crear paneles de control que permiten la visualización detallada de las condiciones ambientales del cultivo.

[![images.png](https://i.postimg.cc/5Nx27P08/images.png)](https://postimg.cc/t7Mb7NFg)

* **MQTT:**  Es un protocolo de mensajería ligero y de bajo consumo de ancho de banda diseñado para dispositivos con recursos limitados y redes con ancho de banda limitado.

[![images-1.png](https://i.postimg.cc/YCCVsFYX/images-1.png)](https://postimg.cc/WhxXDh9r)

## **Funcionalidades:**

Funcionalidades del software:
1. Captura y Transmisión de Datos: Los sensores capturan en tiempo real datos de temperatura, humedad, CO2 e intensidad lumínica. Estos datos se transmiten de forma inalámbrica a través de LoRa hacia una Raspberry Pi.

2. Procesamiento y Almacenamiento: En Node-RED, los datos capturados por los sensores se almacenan en formato JSON. Estos datos se procesan y se envían a un dashboard, permitiendo la visualización en tiempo real de los parámetros temperatura, humedad, CO2 e intensidad lumínica. Posteriormente, Node-RED utiliza el nodo "influxdb out" para insertar estos datos en una base de datos InfluxDB, garantizando un almacenamiento eficiente y facilitando su consulta y análisis posterior.

3. Visualización y Análisis: En Grafana, se estableció una conexión con InfluxDB para visualizar los datos almacenados en nuestra base de datos. Esta integración permite que Grafana consulte directamente InfluxDB, accediendo a los datos históricos y en tiempo real recopilados por los sensores. Se creó un panel personalizado en Grafana, configurando varias visualizaciones y gráficos que representan los parámetros monitoreados, como temperatura, humedad, CO2 e intensidad lumínica. Este panel ofrece una interfaz interactiva y dinámica, facilitando el análisis y la supervisión de los datos. La conexión y configuración en Grafana se realizaron utilizando las credenciales de acceso y la URL del servidor InfluxDB, asegurando una actualización continua y precisa de la información visualizada en el panel.
  
4. Accesibilidad y Gestión Remota:
El prototipo cuenta con una interfaz proporcionada por Node-RED, la cual es fácil de entender. En el dashboard, se visualizan porcentajes de humedad, temperatura, nivel de batería, dióxido de carbono e intensidad de la luz, además del estado de la bomba (encendida o apagada). Adicionalmente, en Grafana se ha configurado un panel que permite apreciar tanto los datos históricos como los datos en tiempo real, ofreciendo una vista integral y detallada de las variables monitoreadas.

5. Interactúa con el hardware:
* **Sensores y Módulo Transmisor LoRa:** Los sensores capturan los datos de temperatura, humedad, CO2 e intensidad lumínica de manera continua. Estos datos son transmitidos hacia el módulo LoRa(Transmisor).
* **Módulo Receptor LoRa (Raspberry Pi):** La Raspberry Pi actúa como receptor de los datos transmitidos por LoRa. Utilizando Node-RED, los datos recibidos son procesados en tiempo real para su posterior manipulación y almacenamiento.
* **Node-RED y InfluxDB:** Node-RED se encarga de procesar y almacenar eficientemente los datos capturados en una base de datos InfluxDB. Al igual que proporciona un dashboard fácil de entender. Esta integración asegura que los datos estén disponibles para análisis y consulta, facilitando la gestión de grandes volúmenes de información de manera efectiva.
* **Grafana:** Grafana proporciona una interfaz gráfica intuitiva y personalizable para la visualización de datos. Permite observar en tiempo real y analizar históricamente las variables monitorizadas, ofreciendo herramientas avanzadas para la interpretación y presentación de los datos recopilados.

## Módulos,clases y funciones del Transmisor:

Módulos y Bibliotecas Utilizadas:

* **heltec.h:** Biblioteca para interactuar con el hardware de la placa Heltec ESP32 LoRa.
* **images.h:** Archivo de imágenes utilizado para la visualización en el display integrado.
* **OneWire.h:** Biblioteca para la comunicación con dispositivos que utilizan el protocolo OneWire, como el sensor de temperatura DS18B20.
* **DallasTemperature.h:** Biblioteca para la lectura de datos del sensor de temperatura DS18B20.

Variables Globales:

* **spread_factor:** Define el factor de propagación utilizado para la comunicación LoRa.
* **dir_local, dir_destino:** Direcciones locales de los dispositivos para la comunicación LoRa.
* **id_msjLoRa:** ID del mensaje LoRa enviado.
* **dir_envio, dir_remite:** Direcciones del dispositivo emisor y receptor para los mensajes LoRa recibidos.
* **paqueteRcb, paqRcb_ID, paqRcb_Estado:** Variables para almacenar y procesar mensajes LoRa recibidos.
* **serial_msj:** Indicador para activar o desactivar los mensajes por el puerto serial.
* **Variables de pines:** Define los pines utilizados para los sensores, actuadores y otros componentes.
  
Funciones Importantes:

* **setup():** Función de inicialización que configura los pines, la comunicación LoRa, el display y otros componentes.
* **loop():** Función principal que se ejecuta continuamente, maneja el envío y recepción de mensajes LoRa, actualiza los sensores y controla las acciones del sistema.
* **sensorBateria():** Función para leer y calcular el nivel de batería del dispositivo.
* **logo():** Función para mostrar un logo en el display integrado al inicio.
* **pantalla_Mostrar():** Función para mostrar datos en el display integrado, como el nivel de batería y otros parámetros ambientales.
* **sensor_revisa():** Función que se encarga de leer los valores de los sensores conectados al sistema y actualizar las variables correspondientes con esos valores.
* **recibe_lora():** Función que  se encarga de procesar los mensajes recibidos a través del módulo LoRa.
envia_lora():Función que se encarga de enviar un paquete LoRa con los datos especificados a través del módulo LoRa.

[![1.png](https://i.postimg.cc/pV3R3zvX/1.png)](https://postimg.cc/7b1F2Cbp)

Módulos,clases y funciones del Receptor:

Módulos y Bibliotecas Utilizadas:
* **Heltec.h:** Utilizada para manejar el hardware específico de los dispositivos Heltec, como la pantalla OLED y el módulo LoRa.
* **WiFi.h:** Utilizada para conectarse a una red WiFi.
* **PubSubClient.h:** Utilizada para manejar las conexiones y las publicaciones/subscripciones MQTT.
  
Variables Globales:

* **BAND:** Define la banda de frecuencia LoRa (915 MHz en este caso).
* **spread_factor:** Define el factor de dispersión para la comunicación LoRa.
* **paqueteEnv, dir_local, dir_destino, msjContador:** Utilizados para manejar los mensajes LoRa a enviar.
* **dir_envio, dir_remite, paqueteRcb, newPaquetesReceb, paqrcbID, paqrcbEstado:** Utilizados para manejar los mensajes LoRa recibidos.
* **rssi_lora, snr_lora:** Almacenan el valor RSSI y SNR del último paquete LoRa recibido.

WiFi y MQTT Variables:

* **ssid, password:** Credenciales para conectarse a la red WiFi.
* **MQTT_IP, MQTT_puerto, MQTT_usuario, MQTT_contrasena:** Credenciales y configuración para conectarse al servidor MQTT.
* **MQTT_ID, MQTT_TOPIC_D1, MQTT_TOPIC_D2, MQTT_TOPIC_D3, MQTT_TOPIC_D4, MQTT_TOPIC_D5:** Identificadores y tópicos para las publicaciones MQTT.
* **MQTT_SensorEstado, mqtt_desconectado, MQTT_COMMAND, MQTT_ActuadorEstado, actuador_estado, actuador_bandera:** Variables para manejar el estado de las conexiones y publicaciones MQTT.
* **wificlient:** Cliente WiFi utilizado por PubSubClient.
* **mqttclient:** Cliente MQTT.
  
Funciones Importantes:

* **void logo():** Muestra el logo en la pantalla OLED.
* **void Presentacion():** Muestra información de conexión en la pantalla OLED.
* **void setup():** Configura el dispositivo, inicializa la pantalla OLED, establece la conexión WiFi y MQTT, y configura el módulo LoRa.
* **void envia_lora(byte destino, byte remite, byte paqueteID, String paquete):** Envía un paquete LoRa con los datos especificados.
* **void recibirlora(int tamano):** Procesa un paquete LoRa recibido.
* **void inicia_wifi():** Establece la conexión WiFi al punto de acceso especificado.
* **void inicia_mqtt():** Establece la conexión al servidor MQTT y configura el cliente MQTT.
* **void publica_estado():** Publica el estado actual del dispositivo en el servidor MQTT.
* **void recibirmqtt(char* p_topic, byte* p_payload, unsigned int p_length):** Maneja los mensajes MQTT recibidos y los procesa adecuadamente.

[![2.png](https://i.postimg.cc/d0W8wFwv/2.png)](https://postimg.cc/FfLfV2Yn)
  
Gateway IoT 

Para nuestro Gateway IoT, es necesario contar con una Raspberry Pi previamente configurada con el sistema operativo Raspbian. Utilizaremos contenedores proporcionados por la aplicación IOTstack para la instalación de los servicios necesarios para nuestro proyecto, incluyendo Node-RED, Grafana e InfluxDB.

1. Descarga y ejecución del menú de IOTstack:
* bash
* cd ~/IOTstack
* ./menu.sh

2 .Selecciona los contenedores deseados del catálogo proporcionado para su instalación.

3. Una vez instalados, activa los contenedores con el siguiente comando:

* cd ~/IOTstack
* docker-compose up -d

Instalación y Configuración de Mosquitto

Para utilizar el servicio Mosquitto, primero debemos asegurarnos de que estamos utilizando el sistema operativo Raspbian Buster.
* lsb_release -a

Agregar el Repositorio de Mosquitto
Importa la llave del repositorio y agrega el repositorio Mosquitto correspondiente a tu versión de Raspbian.

* wget http://repo.mosquitto.org/debian/mosquitto-repo.gpg.key
* sudo apt-key add mosquitto-repo.gpg.key
* cd /etc/apt/sources.list.d/
* sudo wget http://repo.mosquitto.org/debian/mosquitto-buster.list

Instalación de Mosquitto
Instala Mosquitto y los clientes de Mosquitto.

* sudo apt install mosquitto mosquitto-clients

Configuración y Prueba de Mosquitto
Para que MQTT se inicie automáticamente al reiniciar la Raspberry Pi:

* sudo systemctl enable mosquitto

[![shopping.webp](https://i.postimg.cc/Gmv4XCHz/shopping.webp)](https://postimg.cc/FYsFKwbJ)

Node-Red:

Node-RED tiene como objetivo recibir datos de un sensor LoRa a través de MQTT, procesarlos y mostrarlos en un tablero de usuario, además de almacenar estos datos en una base de datos InfluxDB. 
* **Nodo mqtt in:** Este nodo se suscribe al tema LoRa_D4/Cultivos en el broker MQTT y recibe mensajes.
* **Nodo json:** Convierte la carga útil del mensaje MQTT de formato JSON a un objeto JavaScript.
* **Nodo debug:** Muestra los datos recibidos en la consola de depuración de Node-RED.
* **Nodo function:** Este nodo descompone el objeto JSON recibido en mensajes individuales para cada métrica. La función es la siguiente:
  
[![3.png](https://i.postimg.cc/YSfbKZyz/3.png)](https://postimg.cc/bGrQ1CPZ)

* **Nodos ui_gauge, ui_chart, ui_text:** Estos nodos muestran las diferentes métricas en el tablero de usuario. Los datos se presentan en forma de medidores, gráficos y texto.
* **Nodos influxdb out:** Estos nodos envían los datos de cada métrica a una base de datos InfluxDB para almacenamiento y análisis posterior. Cada nodo corresponde a una métrica específica.
* **Nodos ui_spacer:** Espaciadores para organizar los elementos en el tablero.

[![4.png](https://i.postimg.cc/65xsKJMD/4.png)](https://postimg.cc/8s4Xd3QH) 

Grafana:
Grafana es una herramienta poderosa para la visualización de datos y el monitoreo de sistemas. 

1. Instalación de Grafana:
 * Descarga e instala Grafana desde el sitio web oficial.
2. Conexión a la base de datos de InfluxDB:
 * Abre la interfaz web de Grafana y ve al panel de configuración.
 * Agrega una nueva fuente de datos, selecciona InfluxDB y proporciona la información de conexión correspondiente a tu configuración de InfluxDB en Node-RED.
3. Creación de paneles:
 * Una vez conectado a InfluxDB, comienza a crear paneles en Grafana.
 * Haz clic en "Crear" y elige el tipo de panel (gráfico de líneas, barras, tabla, etc.).
 * Configura la consulta para seleccionar los datos que deseas visualizar desde InfluxDB.
4. Personalización y configuración avanzada:
 * Personaliza la apariencia y la configuración del panel según tus necesidades.
 * Añade múltiples series de tiempo, ajusta los ejes, define alertas y realiza otras configuraciones avanzadas para lograr visualizaciones efectivas de tus datos.

[![5.jpg](https://i.postimg.cc/2yhtcDKd/4.jpg)](https://postimg.cc/dZQn3zvD)

# Resultado final

[![1.jpg](https://i.postimg.cc/TY820Bhc/1.jpg)](https://postimg.cc/yWPzYQmJ)

[![2.jpg](https://i.postimg.cc/rp9t2MRc/2.jpg)](https://postimg.cc/8FjCh8bn)

## **Instalación**
1 . Clonar el repositorio:
* Clona este repositorio en tu máquina local.
  
2 .Importar códigos de Arduino:
* Importa los códigos para el Transmisor y el Receptor de Arduino.
  
3 .Importar flujo de Node-RED:
* Importa el flujo de Node-RED.
  
4 .Configurar archivos:
* Configura los archivos .INO y el flujo de Node-RED con tus datos específicos.

5. Ejecutar Sketch y flujo:
* Ejecuta los Sketch de Arduino y el flujo en Node-RED.


