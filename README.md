Cliente/Navegador
      |
      v
+----------------------+
|     Nginx Balancer    |
| http://localhost:8081 |
+----------------------+
      |          |
      v          v
+---------+   +---------+
|  web1   |   |  web2   |
|  :80    |   |  :80    |
+---------+   +---------+



## Cómo ejecutar la infraestructura


docker compose up -d --force-recreate

Para detener:

docker compose down

URL del balanceador

http://localhost:8081

Evidencia Round Robin (10 requests)
1..10 | % { curl.exe -s http://localhost:8081 | findstr "Hola mundo" }


Salida (ejemplo real):

<h1>Hola mundo desde server 1</h1>
<h1>Hola mundo desde server 2</h1>
<h1>Hola mundo desde server 1</h1>
<h1>Hola mundo desde server 2</h1>
<h1>Hola mundo desde server 1</h1>
<h1>Hola mundo desde server 2</h1>
<h1>Hola mundo desde server 1</h1>
<h1>Hola mundo desde server 2</h1>
<h1>Hola mundo desde server 1</h1>
<h1>Hola mundo desde server 2</h1>
