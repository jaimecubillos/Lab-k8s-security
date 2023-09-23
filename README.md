# LABORATORIO SEGURIDAD EN KUBERNETES A NIVEL DE CONTAINER/POD

## PARTE 1 - CONTAINER INMUTABLE

Crear un deployment con el nombre *inmutable* con las siguientes especificaciones:

- Image: busybox
* replicas: 3
+ namespace: secure
- command: sleep 5 min
* container name: secure
+ el container no debe permitir escribir en los archivos root (inmutable)
- Crear un archivo en /etc y /tmp es posible?

## PARTE 2 - NON-ROOT CONTAINER

Crear un deployment con el nombre *non-root* con las siguientes especificaciones:

- Image: httpd:latest
+ namespace: secure
- container name: non-root
* el container no debe correr con usuario root
+ el container dene correr con el usuario con menos privilegios posible 

## PARTE 3 -   NO-PERMISOS PARA ESCALAR PRIVILEGIOS

Crear un deployment con el nombre *privilege* con las siguientes especificaciones:

- Image: busybox
* replicas: 4
+ namespace: secure
- container name: no-provilege
* el container no debe permitir escalar privilegios por medio de sudo u otra técnica

## PARTE 4 - DESHABILITAR SHELL CONSOLE IN PODs

Crear un deployment con el nombre *non-shell* con las siguientes especificaciones:

- Image: nginx
* replicas: 2
+ namespace: secure
- container name: no-shell
- Agregar un startup probe con el comando date
* el container no debe permitir entrar a la consola del pod con kubectl exec -it


