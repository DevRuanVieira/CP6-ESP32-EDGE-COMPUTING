# Projeto de Monitoramento com ESP32, DHT11 e LDR

Este projeto utiliza um ESP32 para monitorar a temperatura, umidade e luminosidade ambiente. Os sensores DHT11 e LDR são usados para coletar os dados, que são enviados via MQTT para um dashboard desenvolvido em Node-RED. O objetivo é criar um sistema simples de monitoramento e visualização em tempo real.

## 🛠 Componentes Utilizados

- **ESP32**: Microcontrolador com conectividade Wi-Fi e Bluetooth.
- **DHT11/DHT22**: Sensor de umidade e temperatura.
- **LDR**: Sensor de luminosidade.
- **Resistor de 10kΩ**: Para o circuito do sensor de luminosidade (LDR).
- **Broker MQTT**: Para receber os dados publicados pelo ESP32.
- **MQTT Client**: Para visualizar os dados (pode ser qualquer aplicativo ou plataforma que suporte MQTT, como MQTT Explorer, Node-RED, ou até mesmo um script Python).
- **Cabo USB**: Para conectar o ESP32 ao computador.
- **Protoboard e Jumpers**: Para montagem dos circuitos.

![image](https://github.com/user-attachments/assets/776b6140-20cc-4130-9f2b-b3d76044a706)


## 📚 Bibliotecas Utilizadas

As bibliotecas a seguir são necessárias para a configuração do ESP32 e leitura dos sensores:

- **DHT Sensor Library**: Utilizada para a leitura de temperatura e umidade.
- **Adafruit Unified Sensor**: Biblioteca de suporte que fornece uma interface comum para todos os sensores Adafruit.
- **PubSubClient**: Utilizada para a comunicação MQTT com o broker.
- **Arduino ESP32 Boards**: Pacote de placas para ESP32, necessário para a programação no Arduino IDE.

## 🚀 Configuração do Projeto

## Biblioteca Necessária

Para rodar o código, você vai precisar das seguintes bibliotecas instaladas no **Arduino IDE** ou na **PlatformIO**:

- **DHT Sensor Library** para leitura de temperatura e umidade.
- **Adafruit Unified Sensor** para suporte aos sensores.
- **PubSubClient** para comunicação MQTT.
- **Arduino** ESP32 Boards

## Esquema de Conexão

### DHT11/DHT22:
- **VCC**: 3.3V do ESP32
- **GND**: GND do ESP32
- **DATA**: GPIO (Ex: D4)

### LDR (Sensor de Luminosidade):
- Um terminal do **LDR** conectado ao **VCC** (3.3V do ESP32).
- O outro terminal do **LDR** conectado a um **resistor de 10kΩ** que vai para o **GND**.
- O ponto comum entre o LDR e o resistor vai ao pino analógico (Ex: A0) do **ESP32**.

![image](https://github.com/user-attachments/assets/780fa22c-0896-456a-b877-5ed933952e11)



### 3. Configuração do Node-RED

#### Instalação do Node-RED

Para instalar o Node-RED, execute os comandos abaixo:

```bash
npm install -g --unsafe-perm node-red
```

Para iniciar o NODE-RED: 

```bash
node-red
```



## Instalação do Broker MQTT

1. **Configuração do Broker MQTT**: 
   - Escolha um broker MQTT (como o **Mosquitto** ou um serviço na nuvem como o **HiveMQ**).
   - Configure o endereço IP e a porta do broker no código.

2. **Instalar Bibliotecas**:
   - No Arduino IDE, vá para "Sketch" > "Incluir Biblioteca" > "Gerenciar Bibliotecas" e instale as bibliotecas mencionadas acima.


3. **Upload do Código**:
   - Conecte o ESP32 ao computador via USB.
   - Faça o upload do código ajustando os parâmetros MQTT e as credenciais Wi-Fi.



![image](https://github.com/user-attachments/assets/c7f558e2-d0fe-4f5a-bdc8-4d60e6c775f3)


## 👥 Integrantes do Grupo 

- Ruan Melo, RM: 557599
- Rodrigo Jimenez RM: 558148
- Pedro Josué RM: 554913
- Lucca Saraiva Borges RM:554608



