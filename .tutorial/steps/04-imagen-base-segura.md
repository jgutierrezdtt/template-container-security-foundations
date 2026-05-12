# Paso 4. Imagen base segura

## Objetivo de aprendizaje

Definir una imagen más segura y reducir privilegios innecesarios.

## Archivo y seccion que debes modificar

- Archivo objetivo: `Dockerfile`.
- Seccion donde aplicar el cambio: instrucciones principales del contenedor.
- Resultado esperado: el repositorio incorpora el control de este paso de forma legible y revisable.

## Cambio que debes introducir

Copia este bloque como base y adáptalo al contexto real del repositorio:

```dockerfile
FROM python:3.11-slim
WORKDIR /app
COPY . .
RUN adduser --disabled-password --gecos "" appuser
USER appuser
CMD ["python", "app.py"]
```

## Como adaptarlo correctamente

- Si el paso es sobre imagen base segura, evita tags genéricos como latest.
- Si el paso es sobre secretos, no uses ARG o ENV para credenciales persistentes.

## Que valida el workflow automaticamente

- `validate-steps.yml` se ejecuta con `push`, `pull_request` y `workflow_dispatch`.
- `scripts/validate-step-04.py` comprueba el archivo y los marcadores esperados de este paso.
- Debe encontrar el marcador `FROM python:3.11-slim` en `Dockerfile`.
- Debe encontrar el marcador `WORKDIR /app` en `Dockerfile`.
- Debe encontrar el marcador `USER appuser` en `Dockerfile`.

## Criterio de finalizacion

El paso 4 queda completado cuando el workflow de GitHub Actions valida este cambio sin errores.

Siguiente paso: Paso 5.
