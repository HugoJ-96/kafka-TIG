# Servidor

- Aquí se va hacer la configuración del servidor para probar la raspberry, primero en PC y despues en el servidor

### Pruebas realizadas:

- Dentro del pc 
- RPI a PC

## server

En este directorio se tiene la arquitectura principal del proyecto:

- En este orden: 

1. Un productor de kafka que en un script de python (en la RPB4) 

2. Los datos van a kafka 

3. Se consumen por telegraf 

4. Se lleva a influxDB como base de datos 

5. finalmente Grafana

### comando para correr:

1. docker-compose up -d (levantar contenedor)

2. docker-compose down (para bajar)

### Configuraciones importantes a revisar:

#### Kafka (.yml):

Revisar los puertos de escucha (9092, 9093)

#### Telegraf:

En el archivo de telegraf.conf, revisar los topicos

## IMPORTANTE:

Antes de llevar esto al servidor hay que considerar la IP del server y que puertos estan utilizando para evitar coliciones de puertos con los docker probablemete acticvos en el servidor.