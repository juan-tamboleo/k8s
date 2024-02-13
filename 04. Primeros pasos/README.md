# Ejemplo de Pod

En [04_pods.yaml](04_pods.yaml) se encuentra un ejemplo básico de la creación de un pod.

# Primera tarea

1. Lanzar un pod que use Wordpress como imagen.
2. Comprobar que existe el pod y obtener información sobre él.
3. Entrar al pod y ejecutar ls.
4. Usar ``kubectl port-forward {pod} {puerto_host}:{puerto_pod} --address={dirección}`` para poder hacer una conexión al wordpress.

Una vez completado, en [04_wordpress_pod.yaml](04_wordpress_pod.yaml) se puede comprobar una solución.