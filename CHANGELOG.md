# Changelog

Todos los cambios notables de este proyecto se documentan en este archivo.

El formato se basa en [Keep a Changelog](https://keepachangelog.com/es-ES/1.1.0/)
y el proyecto usa [Versionado Semántico](https://semver.org/lang/es/).

## [Unreleased]

### Eliminado

- Logo y material del proyecto de láminas IRAM, espejos de `assets/calculations/` y `test/`, carpetas vacías y carpetas legacy de las skills.

### Cambiado

- Logo del proyecto restablecido en `assets/logo.png` y `assets/logo.svg`, usado en el README.
- Documentación de git (`CONTRIBUTING.md`, plantillas, `.gitignore`) y `README.md` para el motor AEA.
- `skill.json` de las skills, sin referencias a carpetas eliminadas.

## [1.5.0] - 2026-10-22

### Añadido

- Skill `feeder-sizing`: formulario de entrada previo, criterios de caída de 1 %, 3 % y 5 %, búsqueda con aluminio y, si no cumple, cobre XLPE.

### Cambiado

- El plugin se llama `aea90364-standard`.

## [1.4.0]

### Añadido

- Memoria de Cálculo (`_MC.md`) y Síntesis de Proyecto (`_SP.md`) del alimentador principal del tablero.
- Opción `--alimentador TAG` en `aea_pipeline.py`.

## [1.3.0]

### Cambiado

- Toda la salida de cálculo va a un único JSON (`<proyecto>_calculo.json`), sin PDF.
- Identificadores de código en inglés; los textos internos siguen en español.
- Skills renombradas: `memoria-calculos` a `calculation-memo` y `sintesis-memoria` a `memo-summary`.

### Eliminado

- Generadores de PDF y todo lo relacionado con gestión de proyectos (CCPM, verificadores documentales, charter y canvas).

El historial anterior del proyecto corresponde a otro generador y no se conserva aquí.
