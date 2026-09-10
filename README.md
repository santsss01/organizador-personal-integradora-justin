# Organizador Personal

## Objetivo

Preparar la estructura inicial de una aplicación que, en el futuro, podría
administrar tareas y notas personales. El foco de esta práctica es el flujo de
trabajo (Visual Studio Code, entorno virtual, dependencias, Git y GitHub), no la
programación.

## Tecnologías utilizadas

- Python 3.14
- Entorno virtual `venv`
- Git y GitHub
- Visual Studio Code
- Bibliotecas: `requests`, `python-dotenv`

## Pasos de instalación

1. Clonar el repositorio:
   ```
   git clone https://github.com/justin12f/organizador-personal-integradora-justin.git
   cd organizador-personal-integradora-justin
   ```
2. Crear y activar el entorno virtual:
   ```
   python -m venv .venv
   .venv\Scripts\activate      # Windows
   source .venv/bin/activate    # Linux / macOS
   ```
3. Instalar las dependencias:
   ```
   pip install -r requirements.txt
   ```
4. Ejecutar el proyecto:
   ```
   python src/main.py
   ```

## Dependencias

Registradas en `requirements.txt` (generado con `pip freeze`):

- `requests` — peticiones HTTP.
- `python-dotenv` — carga de variables de entorno desde un archivo `.env`.

## Estado

Proyecto en fase inicial. Está lista la estructura de carpetas, la
documentación base, el entorno virtual y el registro de dependencias. Aún no
se implementa la lógica de la aplicación; el siguiente paso es la colaboración
mediante fork y Pull Request.

## Colaboración

Este repositorio forma parte de la práctica integradora de Git y GitHub. La
colaboración se realiza mediante **fork y Pull Request**:

1. La persona colaboradora hace un *fork* del repositorio original.
2. Clona su fork y crea una rama de trabajo (`mejora-documentacion`).
3. Realiza sus aportaciones en esa rama y las sube a su fork con `push`.
4. Abre un *Pull Request* hacia la rama `main` del repositorio original.
5. La persona propietaria revisa el Pull Request y usa *Approve* o
   *Request changes* antes de hacer el *merge*.
6. Tras el *merge*, la persona propietaria sincroniza su repositorio local con
   `git pull origin main`.

Aportaciones de esta ronda: se agregó `docs/recomendaciones.md` con
recomendaciones de mejora y esta sección de colaboración en el `README.md`.
Colaboradora: `santsss01`.

## Autor

Justin Emiliano Rodríguez Franco (`justin12f`)
