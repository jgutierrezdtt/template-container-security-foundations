# Paso 10. Medalla final container foundations

## Objetivo de aprendizaje

Explicar qué vulnerabilidades aparecen en la imagen y cómo se priorizan.

## Archivo y seccion que debes modificar

- Archivo objetivo: `docs/container-findings.md`.
- Seccion donde aplicar el cambio: reporte de riesgos del contenedor.
- Resultado esperado: el repositorio incorpora el control de este paso de forma legible y revisable.

## Cambio que debes introducir

Copia este bloque como base y adáptalo al contexto real del repositorio:

```markdown
## Imagen analizada
## CVEs principales
## Riesgo operativo
## Siguiente accion
```

## Como adaptarlo correctamente

- Diferencia vulnerabilidades del sistema base y de dependencias de aplicación.
- Prioriza primero las CVEs explotables en runtime.

## Que valida el workflow automaticamente

- `validate-steps.yml` se ejecuta con `push`, `pull_request` y `workflow_dispatch`.
- `scripts/validate-step-10.py` comprueba el archivo y los marcadores esperados de este paso.
- Debe encontrar el marcador `## Imagen analizada` en `docs/container-findings.md`.
- Debe encontrar el marcador `## CVEs principales` en `docs/container-findings.md`.
- Debe encontrar el marcador `## Riesgo operativo` en `docs/container-findings.md`.
- Debe encontrar el marcador `## Siguiente accion` en `docs/container-findings.md`.

## Criterio de finalizacion

El paso 10 queda completado cuando el workflow de GitHub Actions valida este cambio sin errores.

Este es el ultimo paso del tutorial.
