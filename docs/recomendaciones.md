# Recomendaciones de mejora

Revisión externa del proyecto **Organizador Personal** (colaboradora: `santsss01`).
A continuación se listan sugerencias para fortalecer la estructura y la
documentación del repositorio.

## 1. Agregar un ejemplo de archivo de entorno (`.env.example`)

El proyecto ya incluye `python-dotenv` como dependencia y `.env` está en el
`.gitignore`, pero no hay una plantilla que indique qué variables espera la
aplicación. Se recomienda crear un archivo `.env.example` versionado con las
claves esperadas (sin valores reales), por ejemplo:

```
API_URL=
API_TOKEN=
```

Así cualquier persona que clone el repositorio sabe qué configurar.

## 2. Unificar la versión de Python en la documentación

`README.md` indica *Python 3.14* mientras que el entorno de desarrollo puede
estar en otra versión. Conviene declarar una versión mínima soportada (por
ejemplo *Python 3.12+*) y, opcionalmente, añadir un archivo `.python-version`
para que la herramienta de entorno seleccione el intérprete correcto de forma
automática.

## 3. Añadir una sección "Cómo contribuir" y convención de commits

La documentación describe bien la instalación, pero no explica el flujo de
colaboración. Se recomienda documentar en el `README.md` (o en un
`CONTRIBUTING.md`) los pasos para proponer cambios: hacer fork, crear una rama
descriptiva, escribir mensajes de commit claros en modo imperativo
("Agrega...", "Corrige...") y abrir un Pull Request describiendo qué se agregó,
qué se modificó y qué aporta.

## 4. Incluir evidencia de ejecución en la documentación

Como `src/main.py` solo imprime un mensaje, sería útil mostrar en el `README.md`
la salida esperada al ejecutarlo:

```
$ python src/main.py
Organizador Personal
```

Esto sirve como prueba mínima de que el entorno quedó bien configurado.

## 5. Agregar pruebas automatizadas con `pytest`

El proyecto no cuenta con pruebas. Se recomienda crear una carpeta `tests/` con
un test mínimo que verifique la salida de `src/main.py`, y registrar `pytest`
en `requirements.txt`. Por ejemplo, `tests/test_main.py`:

```python
import subprocess
import sys


def test_main_imprime_titulo():
    resultado = subprocess.run(
        [sys.executable, "src/main.py"],
        capture_output=True,
        text=True,
    )
    assert resultado.stdout.strip() == "Organizador Personal"
```

Se ejecuta con `pytest` desde la raíz del proyecto. Aunque la práctica no se
centra en programar, tener una prueba automatizada básica documenta el
comportamiento esperado y facilita detectar regresiones cuando el proyecto
crezca.
