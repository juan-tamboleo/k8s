# Persistent Volume Claim
- Un PVC es una solicitud de almacenamiento realizada por un pod en Kubernetes.
- Un PVC representa la cantidad de almacenamiento y las características (por ejemplo, modo de acceso, modos de almacenamiento) que un pod necesita para su persistencia.

En el fichero [07_alpine.yaml](07_alpine.yaml) se detalla como se debe utilizar un pvc junto a un ConfigMap, para que un service y un deployment se puedan comunicar.

# ConfigMap
- Un ConfigMap es un recurso en Kubernetes que permite almacenar datos de configuración, como pares clave-valor, archivos de configuración o cualquier dato de configuración que un contenedor pueda necesitar.

Un ejemplo de ConfigMap se puede encontrar en [07_configmap_alpine.yaml](07_configmap_alpine.yaml).

# Tarea
1. Añadir un ConfigMap para configurar wordpress y mariadb y que se pueden comunicar.
2. Añadir un pvc a mariadb.
3. Comprobar que aunque se borre el pod de mariadb la información cuando el pod vuelve sigue.

**IMPORTANTE**
- En envs de wordpress para que pueda acceder:
    - ``WORDPRESS_DB_PASSWORD = root``
    - ``WORDPRESS_DB_USER = root``
- Como mountPath utilizar /var/lib/mysql.