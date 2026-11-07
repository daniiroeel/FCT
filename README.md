Repositorio de Docker y Ansible
1. Descripción del repositorio

Este repositorio tiene como finalidad facilitar al profesorado el acceso y la visualización de los archivos y configuraciones generados durante el desarrollo de la práctica de FCT.

En él se recoge la estructura de los diferentes contenedores desplegados mediante Docker, así como los playbooks y archivos de configuración utilizados para la automatización de tareas mediante Ansible.

El repositorio se organiza en dos directorios principales:

docker/: contiene los archivos relacionados con los contenedores Docker.
ansible/: contiene los archivos relacionados con la automatización mediante Ansible.
2. Estructura del repositorio

La estructura general del repositorio es la siguiente:


├── docker/
│   ├── contenedor1/
│   │   ├── docker-compose.yml
│   │   └── .env
│   │
│   ├── contenedor2/
│   │   └── docker-compose.yml
│   │
│   └── contenedor3/
│       ├── docker-compose.yml
│       └── .env
│
└── ansible/
    └── playbook.yml
    └── inventory.yml
    └── group_vars
        └── all
            └── conexion.yml
            └── usuarios.yml

2.1. Directorio docker/

Este directorio contiene una carpeta independiente para cada uno de los contenedores Docker desplegados.

Dentro de cada carpeta se encuentran los archivos necesarios para definir y configurar el correspondiente servicio:

docker-compose.yml: define los servicios, imágenes, redes, volúmenes y demás parámetros necesarios para desplegar los contenedores.
.env: cuando existe, contiene las variables de entorno utilizadas por Docker Compose, incluyendo los parámetros de configuración correspondientes.

Por motivos de seguridad, los archivos .env incluidos en este repositorio utilizan credenciales modificadas o ficticias, evitando así la exposición de contraseñas y otros datos sensibles.

2.2. Directorio ansible/

Este directorio contiene los archivos relacionados con la automatización mediante Ansible.

Actualmente incluye el playbook encargado de la creación de usuarios locales en sistemas Windows, utilizando Ansible y WinRM como mecanismo de conexión y administración remota.

El playbook permite automatizar la generación de usuarios a partir de una lista de variables que contiene sus datos personales y nombres de usuario.

3. Consideraciones de seguridad

Los archivos compartidos en este repositorio tienen una finalidad demostrativa y documental.

Se han tenido en cuenta las siguientes medidas:

Las contraseñas y credenciales reales han sido sustituidas por valores ficticios.
No se incluyen claves privadas ni tokens de acceso.
Los archivos de configuración se comparten con fines de revisión y consulta por parte del profesorado.
