
# JARVIS MODULO CAIXA DAGUA

Utilizado 03 sensores de nível de água para leitura do nível de água.

## CONFIGURAÇÃO DO MÓDULO
- ID - 5  
- Sensor Nivel de agua: id 10

### CODIGOS
- 100 - msg hello
- 200 - msg de leitura de sensores

{
    "code": 200,
    "idSensor": 1005,
    "description": "nivel de agua da caixa dagua",
    "cheio": false,
    "meio": false,
    "vazio": false
}

## FUNCOES DOS SENSORES
faz a leitura dos sensores:  
readSensorCheio()  
readSensorMeio()  
readSensorVazio()  

## CONFIGURAÇÕES REDE MESH
- ID: ID do módulo no projeto JARVIS  
- STATION_SSID: nome da rede wifi  
- STATION_PASSWORD: senha da rede wifi  
- STATION_CHANNEL: canal do AP (necessário configurar o AP local para canal fixo)  

## FUNÇÕES REDE MESH
getMessageHello(JsonDocument myObject); imprime as msg hello recebidas  
sendMessageHello(); envia msg hello a cada 11s  
checkConnection(); reinicia o ESP se perder conexao a rede mesh  

sendSensorReandingNivelCaixaDagua(); envia a leitura dos sensores a cada 5s  

## Observações:
- Somente um dispositivo pode ser o nó raiz na malha (root)  
- Configurar o SSID e Senha da Rede WIFI Local
- Configurar Roteador WIFI para canal Manual, o mesmo canal do AP deve ser configurado em todos os dispositivos pertencentes a rede mesh

## Referências
https://github.com/jackson-veloso/ESP32_WATCHDOG  
https://github.com/jackson-veloso/ESP32_REDE_MESH_PAINLESSMESH  
https://github.com/jackson-veloso/JARVIS-Modulo-ESP32-Client  
https://github.com/jackson-veloso/ESP32_EFEITO_BOUCING  

https://blog.eletrogate.com/criando-uma-rede-mesh-com-os-modulos-esp-8266-esp-32-esp-01/  
https://randomnerdtutorials.com/esp-mesh-esp32-esp8266-painlessmesh/  
https://gitlab.com/painlessMesh/painlessMesh  
https://www.fernandok.com/2018/06/travou-e-agora.html  
https://labdegaragem.com/forum/topics/esp32-travou-e-agora  
https://www.blogdarobotica.com/2021/05/24/entenda-o-efeito-bounce-e-como-fazer-debounce-no-arduino-ao-apertar-um-botao/  
https://blog.eletrogate.com/o-que-e-o-efeito-bouncing-e-como-evita-lo/  
https://www.usinainfo.com.br/blog/sensor-de-nivel-de-agua-com-arduino-automacao-residencial-de-controle/  
