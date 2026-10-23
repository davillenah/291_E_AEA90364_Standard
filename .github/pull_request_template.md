## Resumen

<!-- Qué cambia en el cálculo y por qué. Citar la cláusula de la norma. -->

## Tipo de cambio

- [ ] Nueva fórmula, tabla o norma
- [ ] Corrección de cálculo
- [ ] Cambio en skill o en documentos (MC o SP)
- [ ] Documentación
- [ ] Versión / release

## Checklist

- [ ] Las pruebas pasan: `python -m unittest discover -s . -p "test_*.py"` en `library/calculations/`
- [ ] Claves del JSON (`In`, `Ib`, `icu`, `S`, `dU`, `disp`) sin cambios, o cambio MAJOR documentado
- [ ] `src/input_for_sld_V1.xlsx` sin modificar
- [ ] Salida regenerada, sin avisos inesperados
- [ ] Módulos copiados a `plugin/elec-calc-generator/scripts/`
- [ ] Versión actualizada en los dos `plugin.json`
- [ ] `CHANGELOG.md` actualizado
- [ ] Paquete `plugin/aea90364-standard.plugin` reconstruido
