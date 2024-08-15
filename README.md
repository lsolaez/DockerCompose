# Dockerized Web Services for MIPSTranslator and LogisimWeb

## Descripción

Este proyecto utiliza Docker para desplegar un entorno con tres contenedores que facilitan el acceso a dos aplicaciones web y una página de bienvenida. La solución incluye un proxy inverso (Nginx) para gestionar las solicitudes y redirigirlas a las aplicaciones web correspondientes.

## Tecnologías Utilizadas

- **Contenedores:**
  - ![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
  - ![Nginx](https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white)

- **Aplicaciones Web:**
  - **MIPSTranslator**
  - **LogisimWeb**


## Ejecución del Código
Para ejecutar este proyecto en tu máquina local utilizando Docker, sigue estos pasos:

1. **Instalación de Docker y Docker Compose:**

Si aún no tienes Docker y Docker Compose instalados, puedes descargarlos e instalarlos desde el sitio web oficial de Docker

2. **Clonación del repositorio y configuración del proyecto:**

 - Clona el repositorio en tu máquina local utilizando el siguiente comando
```plaintext
   git clone <URL_del_repositorio>
   cd <nombre_del_directorio>
```

4. **Construcción y ejecución de contenedores:**

  Una vez dentro del directorio del proyecto, construye y levanta los contenedores ejecutando:
```plaintext
docker-compose up --build
```

5. **Acceso a la Aplicación:**

- Navega a http://localhost:8080 para acceder a la página de bienvenida.
- Utiliza los enlaces disponibles para redirigirte a los servicios de los contenedores:
  - /c2/ para el contenedor MIPSTranslator (puerto 8000).
  - /c3/ para el contenedor LogisimWeb (puerto 8001).
 
## Contenedores
- Contenedor 1: Proxy
  Imagen: Nginx
  Puerto Expuesto: 80
  Descripción: Proporciona la página de bienvenida y redirige las solicitudes a los otros contenedores.

- Contenedor 2: MIPSTranslator
  Puerto Expuesto: 8000
  Descripción: Aplicación web basada en el proyecto MIPSTranslator.

- Contenedor 3: LogisimWeb
  Puerto Expuesto: 8001
  Descripción: Aplicación web basada en el proyecto LogisimWeb.
