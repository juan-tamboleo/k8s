# Servicios
- ClusterIP: IP fija dentro del cluster entre todos los Pods a los que se les asigne este servicio.
- NodePort: para exponer la aplicación a un puerto estático.
- LoadBalancer: balanceador de carga externo relacionado con el uso de la nube.

En [06_alpine_service.yaml](06_alpine_service.yaml) se puede encontrar un ejemplo de como desplegar un servicio para un deployment.

# Tarea
1. Crear un servicio para un deployment de wordpress. Este servicio debe ser de tipo ClusterIP.
2. Realizar un servicio para un deployment de mariadb. Este servicio debe ser también de tipo ClusterIP.

En [06_mariadb_service.yaml](06_mariadb_service.yaml) y en [06_wordpress_service.yaml](06_wordpress_service.yaml) se encuentran unas posibles soluciones.