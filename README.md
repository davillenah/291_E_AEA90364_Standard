<div align="center">

<img src="assets/logo.png" alt="aea90364-standard" width="320"/>

# aea90364-standard

</div>


Motor de cálculo de instalaciones de baja tensión según **AEA 90364-7** (771, 770, 701, 722) y **AEA 90909-1**. Se empaqueta como plugin de Claude.

## Qué hace

- Lee el Excel de circuitos (`TABLERO`, `CIRCUITOS`) y calcula cada circuito: corriente de proyecto, In, icu, sección, caída de tensión y protección.
- Exporta todo el cálculo a un único JSON (`<proyecto>_calculo.json`) que consume `sld-generator`.
- Para el alimentador principal del tablero, genera la Memoria de Cálculo (`_MC.md`) y la Síntesis de Proyecto (`_SP.md`). No genera PDF.
- Acepta cargas en A, W, kW, MW, VA, kVA, MVA, HP o CV, y convierte cada una a corriente.

## Uso

```
python library/calculations/aea_pipeline.py src/input_for_sld_V1.xlsx
```

Opciones principales: `-o` (JSON de salida), `--alimentador TAG`, `--margen-iz`, `--eta-motores`, `--temp-c`, `--k-magnetico`.

## Skills

| Skill | Función |
|---|---|
| `feeder-sizing` | Dimensionado paso a paso del alimentador, con formulario de entrada y criterios de caída de 1 %, 3 % y 5 % |
| `electrical-dimensioning` | Flujo completo de dimensionado de la instalación |
| `calculation-memo` | JSON de todos los circuitos y MC del alimentador principal |
| `memo-summary` | SP del alimentador principal |

## Estructura

- `library/calculations/`: código fuente y pruebas.
- `skills/`: skills de trabajo.
- `plugin/elec-calc-generator/`: carpeta del plugin.
- `plugin/aea90364-standard.plugin`: paquete para instalar.
- `assets/`: normas AEA en PDF (referencia).
- `src/`: Excel de entrada y salidas generadas.

## Pruebas

```
cd library/calculations
python -m unittest discover -s . -p "test_*.py"
```

## Contribuir

Ver [CONTRIBUTING.md](CONTRIBUTING.md) y el [Changelog](CHANGELOG.md).
