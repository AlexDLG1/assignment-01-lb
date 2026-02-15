<<<<<<< HEAD
=======
# Load Balancer (Round Robin) - Assignment 01

## Diagrama de la infraestructura

```text
>>>>>>> f3908aa (Create README.md)
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
<<<<<<< HEAD



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



## Notas
- Se utilizó el puerto 8081 porque el 8080 estaba ocupado.
=======
>>>>>>> f3908aa (Create README.md)
