# Load Balancer (Round Robin) - Assignment 01

## Diagrama de la infraestructura

```text
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
Cómo ejecutar la infraestructura
Clonar el repositorio
git clone https://github.com/AlexDLG1/assignment-01-lb.git
cd assignment-01-lb

2) Ejecutar la infraestructura
docker compose up -d --force-recreate

3) Abrir el balanceador

URL: http://localhost:8081

4) Evidencia Round Robin (10 request)
Comando:

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
Notas
Si otra persona quiere probar el proyecto, debe clonarlo y ejecutarlo en su máquina
Se utilizó el puerto 8081 porque el 8080 estaba ocupado.
