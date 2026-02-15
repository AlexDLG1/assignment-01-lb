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
