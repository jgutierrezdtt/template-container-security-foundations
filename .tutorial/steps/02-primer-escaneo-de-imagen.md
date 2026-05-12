# Paso 2. Primer escaneo de imagen

## Objetivo de aprendizaje

Automatizar el análisis de vulnerabilidades del contenedor.

## Archivo y seccion que debes modificar

- Archivo objetivo: `.github/workflows/container-security.yml`.
- Seccion donde aplicar el cambio: workflow de build y escaneo.
- Resultado esperado: el repositorio incorpora el control de este paso de forma legible y revisable.

## Cambio que debes introducir

Copia este bloque como base y adáptalo al contexto real del repositorio:

```yaml
name: Container Security
on:
  pull_request:
  push:
jobs:
  trivy:
    runs-on: ubuntu-latest
```

## Como adaptarlo correctamente

- Separa build y scan si necesitas depurar fallos con claridad.
- Usa una sola herramienta de ejemplo por paso para que el aprendizaje sea incremental.

## Que valida el workflow automaticamente

- `validate-steps.yml` se ejecuta con `push`, `pull_request` y `workflow_dispatch`.
- `scripts/validate-step-02.py` comprueba el archivo y los marcadores esperados de este paso.
- Debe encontrar el marcador `name: Container Security` en `.github/workflows/container-security.yml`.
- Debe encontrar el marcador `pull_request:` en `.github/workflows/container-security.yml`.
- Debe encontrar el marcador `push:` en `.github/workflows/container-security.yml`.
- Debe encontrar el marcador `trivy:` en `.github/workflows/container-security.yml`.

## Criterio de finalizacion

El paso 2 queda completado cuando el workflow de GitHub Actions valida este cambio sin errores.

Siguiente paso: Paso 3.
