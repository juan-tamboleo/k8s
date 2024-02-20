# Kubernetes

## Instalación

- [Docker](https://docs.docker.com/engine/install/ubuntu/#install-using-the-repository)
    -  **IMPORTANTE**: [post-installation](https://docs.docker.com/engine/install/linux-postinstall/)
    1. `sudo groupadd docker`
    2. `sudo usermod -aG docker $USER`
    3. `newgrp docker`
    4. `docker run hello-world`
        - Si este comando se ejecuta sin problemas, ya se tendrían que haber aplicado los cambios 🫡.
- [Kubectl](https://docs.docker.com/engine/install/ubuntu/#install-using-the-repository)
- [Minikube](https://minikube.sigs.k8s.io/docs/start/)

## Comandos

### [Minikube](https://minikube.sigs.k8s.io/docs/commands/)
- START
    - minikube start \[flags\]
    - minikube start -n|--nodes 2
    - **IMPORTANTE**. Utilizar minikube start con la opción --driver=docker. `minikube start --driver=docker`
- STOP
    - minikube stop \[flags\]
- DELETE
    - minikube delete \[flags\]
- SERVICE
    - minikube service \[flags\] {service}

### [kubectl](https://kubernetes.io/docs/reference/generated/kubectl/kubectl-commands)
- GET
    - kubectl get \[flags\]: para obtener información del cluster.
    - ``kubectl get nodes``
    - ``kubectl get namespaces``
    - ``kubectl get pods``
    - ``kubectl get deployments/services...``
    - ``kubectl get {...} -o wide/yaml``
- APPLY
    - kubectl apply \[flags\]: para aplicar configuraciones al cluster.
    - ``kubectl apply -f {ruta/al/fichero}``
- DELETE
    - kubectl delete \[flags\]: para borrar configuraciones del cluster.
    - ``kubectl delete {recurso}``
    - ``kubectl delete -f {ruta/al/fichero}``
- EXEC
    - kubectl exec {recurso} \[flags\] -- {comando}: para ejecutar comandos desde los pods.
    - ``kubectl exec -it {recurso} -- /bin/bash|sh``
- DESCRIBE
    - kubectl describe {recurso} \[flags\]: para obtener información más detallada.
- LOGS
    - kubectl logs {recurso} \[flags\]: para obtener los logs del contenedor de un pod.

Para trabajar con **namespaces** se utiliza la opción `-n {namespace}`.

[Cheatsheet de comandos](https://www.scaleway.com/en/docs/containers/kubernetes/reference-content/kubernetes-cheatsheet/)