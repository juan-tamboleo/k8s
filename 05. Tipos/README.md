# Tipos

## Deployment
- Sirve para declarar el estado deseado de un Pod.
- Gestiona la creación, actualización y escalado de Pods.
- Se crea de forma declarativa.

## DaemonSet
- La definición de un Pod que se haga en DaemonSet se aplicará para que todos los nodos tengan una copia.
- Todos los nodos en el cluster tendrán la misma definición.

## ReplicaSet
- Va a asegurar que siempre va a haber una copia en todo momento.
- Importante para aplicaciones que requieren de alta disponibilidad.

## StatefulSet
- Para aplicaciones que requieren mantener un estado.

# Ejemplo de Deployment
En [05_alpine_deployment.yaml](05_alpine_deployment.yaml) se encuentra un ejemplo sobre la creación de un Deployment con dos Pods.

# Tarea
1. Crear un deployment utilizando la imagen de mariadb y poner el deployment en el namespace web-test
    Se crea un namespace con `kubectl create namespace`
2. Accede al Pod
3. Comprueba la versión de mariadb
4. Obtener el usuario actual con: `mariadb -uroot -p{pass} -e "select current_user()`

**👁️ OJO 👁️**
```yaml
spec:
  containers:
  - name:
    image:
    env:
    - name: MYSQL_ROOT_PASSWORD
      value: root
    - name: MARIADB_DATABASE
      value: wordpress
```

Se puede ver una solución en [05_mariadb_deployment.yaml](05_mariadb_deployment.yaml).